# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

## Objetivo
O objetivo deste projeto é utilizar o Amazon SageMaker Canvas para construir e treinar um modelo de Machine Learning que preveja a quantidade de estoque promocional de produtos.

## Passo a Passo

### 1. Selecionar Dataset

**Seleção do Dataset:**

- O dataset "PrevisaoPromocional" foi selecionado, contendo 1.000 linhas de registros.
- Este dataset inclui as seguintes colunas: `QUANTIDADE_ESTOQUE`, `PRECO`, `ID_PRODUTO`, `FLAG_PROMOCAO`, `DATA_EVENTO`.

**Upload do Dataset:**

- O dataset foi carregado no SageMaker Canvas na aba "Datasets".

### 2. Construir e Treinar

**Importação do Dataset:**

- Dentro do SageMaker Canvas, o dataset "PrevisaoPromocional" foi importado com sucesso.

**Configuração das Variáveis:**

- **Variável de Saída:** `QUANTIDADE_ESTOQUE` (target column).
- **Variáveis de Entrada:** `PRECO`, `ID_PRODUTO`, `FLAG_PROMOCAO`, `DATA_EVENTO`.

**Início do Treinamento do Modelo:**

- O modelo "VendasProdutosPromocionais" foi configurado para prever a quantidade de estoque usando uma abordagem de previsão de séries temporais.
- Configuração de série temporal especificada para 2 dias.
- Um treinamento rápido (Quick Build) foi realizado inicialmente para uma análise preliminar.

### 3. Analisar

**Métricas de Performance:**
- Após o treinamento rápido, o modelo forneceu várias métricas de performance, como precisão, recall e F1-score.
- As principais características que influenciam as previsões foram identificadas e analisadas.

**Ajustes no Modelo:**
- Se necessário, ajustes nas variáveis de entrada ou outros parâmetros do modelo foram realizados.
- O modelo foi re-treinado até alcançar um desempenho satisfatório.

### 4. Prever

**Geração de Previsões:**

- Utilizando o modelo treinado "VendasProdutosPromocionais", foram feitas previsões de estoque.
- Novos datasets foram carregados para gerar as previsões.

**Exportação e Análise dos Resultados:**

- As previsões foram exportadas para um arquivo CSV.
- As previsões geradas foram analisadas, gerando insights sobre a quantidade de estoque promocional prevista para os próximos dias.

## Conclusões

O modelo de previsão forneceu insights valiosos sobre a quantidade de estoque necessária para produtos em promoção. As métricas de performance indicaram um bom desempenho do modelo após ajustes e re-treinamento.
