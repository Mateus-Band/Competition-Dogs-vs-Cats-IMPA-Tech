# PICME – Classificação Cats vs Dogs (Repositório Unificado)

Repositório consolidado reunindo os desenvolvimentos individuais e a documentação comparativa da competição **Cats vs Dogs** do programa **PICME / IMPA Tech** (Processamento de Imagens).

Todos os históricos de commits originais de cada integrante foram preservados neste repositório.

---

## Estrutura do Repositório

| Caminho | Conteúdo | Repositório / Fonte de Origem |
|---|---|---|
| [`AnaliseFinal.ipynb`](./AnaliseFinal.ipynb) | **Notebook de Análise Comparativa Final**: consolida arquiteturas, hiperparâmetros, curvas de aprendizado, métricas de validação/teste, intervalos de confiança e avaliação unificada no banco externo `Pets` (77 imagens) dos 4 modelos | Repositório Unificado (`PICME-Cats-vs-Dogs`) |
| [`Competicao/`](./Competicao/README.md) | Compilação geral da competição: comparativos metodológicos, evolução dos treinamentos, bancos de dados, avaliação externa `Pets` e diagramas padronizados de arquitetura (formato *Understanding Deep Learning*) | [`TheoAmbrosio/picme-processamento-de-imagens`](https://github.com/TheoAmbrosio/picme-processamento-de-imagens) (`Competicao-Cats and dogs/`) |
| [`Theo/`](./Theo/README.md) | Modelo **ResTheo34 Aug8**, linhagem de redes residuais, scripts de ampliação de dados e registros de experimentos do Theo | [`TheoAmbrosio/picme-processamento-de-imagens`](https://github.com/TheoAmbrosio/picme-processamento-de-imagens) (`Cats and Dogs I e II/`) |
| [`Lisandra/`](./Lisandra/README.md) | Classificador CNN **AlexNetBinary**, notebooks de treinamento e pacote de resultados para a competição da Lisandra | [`lisandra21/cats_vs_dogs_Lisandra`](https://github.com/lisandra21/cats_vs_dogs_Lisandra) |
| [`Dulce/`](./Dulce/README.md) | Modelos CNN (**CNN 224 v2** e experimentos com **ResNet18**), histórico de decisões, logs de treinamento e pesos do modelo final da Dulce | [`dulce-costa/Picme2.2Cats_Dogs`](https://github.com/dulce-costa/Picme2.2Cats_Dogs) (`Cats vs Dogs/`) |
| [`Mateus/`](./Mateus/README.md) | Pipeline modular em PyTorch (**CNN V1–V4** e **V4 Final** fine-tuning), scripts de pré-processamento, análises de resultados e pesos dos modelos do Mateus (Bandeira) | [`Mateus-Band/Dogs-vs-Cats-IMPATech`](https://github.com/Mateus-Band/Dogs-vs-Cats-IMPATech) |

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
