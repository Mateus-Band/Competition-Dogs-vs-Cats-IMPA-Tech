# PICME – Classificação Cats vs Dogs (Repositório Unificado)

Repositório consolidado reunindo os desenvolvimentos individuais e a documentação comparativa da competição **Cats vs Dogs** do programa **PICME / IMPA Tech** (Processamento de Imagens).

Todos os históricos de commits originais de cada integrante foram preservados neste repositório.

---

## Estrutura do Repositório

| Caminho | Conteúdo | Repositório / Fonte de Origem |
|---|---|---|
| [`AnaliseFinal.ipynb`](./AnaliseFinal.ipynb) | **Notebook de Análise Comparativa Final**: consolida arquiteturas, hiperparâmetros, curvas de aprendizado, métricas de validação/teste, intervalos de confiança e avaliação unificada no banco externo `Pets` (78 imagens) dos 4 modelos | Repositório Unificado (`PICME-Cats-vs-Dogs`) |
| [`Competicao/`](./Competicao/README.md) | Compilação geral da competição: comparativos metodológicos, evolução dos treinamentos, bancos de dados, avaliação externa `Pets` e diagramas padronizados de arquitetura (formato *Understanding Deep Learning*) | [`TheoAmbrosio/picme-processamento-de-imagens`](https://github.com/TheoAmbrosio/picme-processamento-de-imagens) (`Competicao-Cats and dogs/`) |
| [`Theo/`](./Theo/README.md) | Modelo **ResTheo34 Aug8**, linhagem de redes residuais, scripts de ampliação de dados e registros de experimentos do Theo | [`TheoAmbrosio/picme-processamento-de-imagens`](https://github.com/TheoAmbrosio/picme-processamento-de-imagens) (`Cats and Dogs I e II/`) |
| [`Lisandra/`](./Lisandra/README.md) | Classificador CNN **AlexNetBinary**, notebooks de treinamento e pacote de resultados para a competição da Lisandra | [`lisandra21/cats_vs_dogs_Lisandra`](https://github.com/lisandra21/cats_vs_dogs_Lisandra) |
| [`Dulce/`](./Dulce/README.md) | Modelos CNN (**CNN 224 v2** e experimentos com **ResNet18**), histórico de decisões, logs de treinamento e pesos do modelo final da Dulce | [`dulce-costa/Picme2.2Cats_Dogs`](https://github.com/dulce-costa/Picme2.2Cats_Dogs) (`Cats vs Dogs/`) |
| [`Mateus/`](./Mateus/README.md) | Pipeline modular em PyTorch (**CNN V1–V4** e **V4 Final** fine-tuning), scripts de pré-processamento, análises de resultados e pesos dos modelos do Mateus (Bandeira) | [`Mateus-Band/Dogs-vs-Cats-IMPATech`](https://github.com/Mateus-Band/Dogs-vs-Cats-IMPATech) |
| [`dataset/`](./dataset/) | **Banco de Teste Externo Pets IMPATech**: 78 fotografias reais de animais de estimação da comunidade IMPA Tech (**45 gatos** e **33 cachorros**) usadas no benchmark de generalização fora de domínio | Fotos fornecidas pela turma do PICME |

---

## Resultados da Competição no Banco Externo `Pets` (78 Fotos)

| Posição | Participante | Modelo | Origem dos Pesos | Validação Interna | Acurácia `Pets` | Acurácia Balanceada | F1 Cão | Recall Gato | Queda de Generalização |
| :---: | :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **1º** | **Theo** | `ResTheo34 Aug8` | ImageNet ResNet-34 sem `layer4` | 98,32% | **84,62% (66/78)** | 85,86% | 83,78% | 77,78% | -13,70 p.p. |
| **2º** | **Mateus (Bandeira)** | `CNN V4 Final` | **Do zero** (5 blocos Conv + GAP + Fine-Tuning) | 94,76% | **82,05% (64/78)\*** | **82,42%** | **80,00%** | **80,00%** | **-12,71 p.p. (★ menor queda)** |
| *ref* | *Mateus (Resize Direto)* | *CNN V4 Final* | *Pré-processamento com distorção forçada (384×384)* | *94,76%* | *78,21% (61/78)* | *79,50%* | *77,33%* | *71,11%* | *-16,55 p.p.* |
| **3º** | **Dulce** | `CNN224 v2` | Do zero (5 blocos Conv5×5 + FC densa) | 96,90% | **75,64% (59/78)** | 77,27% | 75,32% | 66,67% | -21,26 p.p. |
| **4º** | **Lisandra** | `AlexNetBinary` | Do zero (5 blocos Conv + BatchNorm + FC 4096) | 90,16% | **61,54% (48/78)** | 62,63% | 60,53% | 55,56% | -28,62 p.p. |

> **(\*) Nota Metodológica:** A avaliação de cada modelo respeita estritamente o seu pré-processamento nativo de treinamento. Para Mateus, preserva-se o aspect ratio (`Resize(384)` proporcional + `CenterCrop(384)`). Quando submetido ao redimensionamento anisotrópico forçado `Resize((384, 384))`, a distorção morfológica das imagens reais retangulares penalizava o modelo para 78,21%. Em seu regime nativo, o modelo treinado do zero atinge 82,05% (apenas 2 acertos de diferença da ResNet com pré-treino ImageNet), lidera no recall de felinos (80,0%) e tem a menor perda de generalização de toda a competição.

---

## Navegação Rápida

- **Notebook Comparativo Consolidado**: [`AnaliseFinal.ipynb`](./AnaliseFinal.ipynb)
- **Visão Geral e Comparação da Competição**: [`Competicao/README.md`](./Competicao/README.md)
  - [Relatório de Performance no Banco Externo `Pets` (77 imagens)](./Competicao/coisas%20para%20apresentacao/Resumo%20publico%20Pets/RELATORIO_PERFORMANCE.md)
  - [Evolução dos Treinamentos](./Competicao/EVOLUCAO_TREINAMENTOS.md)
  - [Bancos de Dados e Preparação](./Competicao/BANCOS_DE_DADOS.md)
  - [Galeria de Slides e Diagramas SVG](./Competicao/coisas%20para%20apresentacao/README.md)
  - [Fontes e Commits Consolidados](./Competicao/FONTES.json)
- **Projetos Individuais**:
  - **Theo**: [`Theo/README.md`](./Theo/README.md) | [Modelo Principal](./Theo/modelo%20principal/README.md)
  - **Lisandra**: [`Lisandra/README.md`](./Lisandra/README.md) | [Resultados da Competição](./Lisandra/resultados_para_competicao/README.md)
  - **Dulce**: [`Dulce/README.md`](./Dulce/README.md) | [Notebooks e Modelo (`Cats vs Dogs/`)](./Dulce/Cats%20vs%20Dogs/)
  - **Mateus (Bandeira)**: [`Mateus/README.md`](./Mateus/README.md) | [Análises V1–Final](./Mateus/Analysis/)
