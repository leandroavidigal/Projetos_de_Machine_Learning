# Projeto de Previsão de Estoque usando Amazon SageMaker

Este projeto tem como objetivo criar um modelo de previsão de estoque utilizando Amazon SageMaker Canvas. O projeto envolve quatro etapas principais: Selecionar Dataset, Construir/Treinar, Analisar e Prever.

## Etapas do Projeto

### 1. Selecionar Dataset

1. Navegue até a pasta `datasets` deste repositório. Esta pasta contém os datasets que você poderá escolher para treinar e testar seu modelo de Machine Learning (ML).
2. Sinta-se à vontade para gerar ou enriquecer seus próprios datasets. Quanto mais você se engajar, mais relevante esse projeto será em seu portfólio.
3. Escolha o dataset que você usará para treinar seu modelo de previsão de estoque.
4. Faça o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

1. No SageMaker Canvas, importe o dataset que você selecionou.
2. Configure as variáveis de entrada e saída de acordo com os dados:
   - **Coluna que identifica exclusivamente os itens:** `ID_PRODUTO`
   - **Coluna que agrupa a previsão pelos valores da coluna:** `FLAG_PROMOCAO`
   - **Coluna que contém os registros de data e hora:** `DATA_EVENTO`
3. Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

Após o treinamento, examine as métricas de performance do modelo:

- **Avg. wQL (Average Weighted Quantile Loss):** `0.523`
  - **Descrição:** A perda quantílica ponderada média é uma métrica que avalia a precisão das previsões em diferentes quantis.
  - **Interpretação:** Um valor de `0.523` indica que, em média, o modelo tem um erro ponderado quantílico de 0.523. Isso sugere que o modelo tem uma precisão razoável nas previsões.

- **MAPE (Mean Absolute Percentage Error):** `1.251`
  - **Descrição:** O erro percentual absoluto médio mede a precisão das previsões ao calcular a média dos erros percentuais absolutos entre os valores previstos e os reais.
  - **Interpretação:** Um MAPE de `1.251` (ou 125.1%) é relativamente alto, indicando que, em média, as previsões do modelo estão erradas por 125.1% em relação aos valores reais.

- **WAPE (Weighted Absolute Percentage Error):** `0.772`
  - **Descrição:** O erro percentual absoluto ponderado é similar ao MAPE, mas leva em consideração o peso das observações.
  - **Interpretação:** Um WAPE de `0.772` (ou 77.2%) sugere que, em média, o erro absoluto ponderado é de 77.2% dos valores reais.

- **RMSE (Root Mean Squared Error):** `33.900`
  - **Descrição:** O erro quadrático médio raiz é uma métrica que mede a média das diferenças ao quadrado entre os valores previstos e os reais.
  - **Interpretação:** Um RMSE de `33.900` indica que a média das diferenças ao quadrado entre as previsões e os valores reais é de 33.900. Valores mais baixos indicam um modelo mais preciso.

- **MASE (Mean Absolute Scaled Error):** `0.884`
  - **Descrição:** O erro absoluto médio escalado é uma métrica que compara o erro absoluto médio do modelo com o erro absoluto médio de uma técnica de benchmark.
  - **Interpretação:** Um MASE de `0.884` menor que 1 indica que o modelo é melhor que a técnica de benchmark. Valores menores que 1 são desejáveis.

### Análise dos Gráficos de Previsão

#### Item `1007` com `FLAG_PROMOCAO` = 1

- **Demanda Histórica (Linha Azul):** A linha azul mostra grandes flutuações na demanda histórica do item `1007` antes de 7 de fevereiro de 2024, com picos notáveis nos dias 2 e 4 de fevereiro.
- **Previsões (Linhas Rosa, Verde e Dourada):**
  - **P10 (Linha Rosa):** Mostra previsões de estoque mais baixas.
  - **P50 (Linha Verde):** Mostra a previsão mediana de estoque.
  - **P90 (Linha Dourada):** Mostra previsões mais altas de estoque.

#### Item `1007` com `FLAG_PROMOCAO` = 0

- **Demanda Histórica (Linha Azul):** A linha azul mostra grandes flutuações na demanda histórica do item `1007` antes de 7 de fevereiro de 2024.
- **Previsões (Linhas Rosa, Verde e Dourada):**
  - **P10 (Linha Rosa):** Mostra previsões de estoque mais baixas.
  - **P50 (Linha Verde):** Mostra a previsão mediana de estoque.
  - **P90 (Linha Dourada):** Mostra previsões mais altas de estoque.

### Conclusões

1. **Variabilidade na Demanda:**
   - A demanda histórica tem mostrado grandes variações, refletidas nas previsões com diferentes quantis (P10, P50, P90).

2. **Tendência de Previsão:**
   - As previsões medianas (P50) indicam uma estabilidade relativa no valor do estoque, com flutuações moderadas.
   - A alta variação entre os quantis P10 e P90 destaca a incerteza na demanda futura.

3. **Relevância da Promoção:**
   - Com `FLAG_PROMOCAO` definida como `1`, é esperado que a demanda aumente durante o período de previsão.
   - Comparado ao cenário com `FLAG_PROMOCAO` = 0, as previsões de estoque são mais altas e mais voláteis quando a promoção está ativa.

### 4. Prever

1. Use o modelo treinado para fazer previsões de estoque.
2. Exporte os resultados e analise as previsões geradas.
3. Documente suas conclusões e qualquer insight obtido a partir das previsões.

## Estrutura do Repositório
├── datasets
│ ├── dataset1.csv
│ └── dataset2.csv
├── README.md
└── scripts
├── train_model.py
└── analyze_results.py


## Ferramentas Utilizadas

- **Amazon SageMaker:** Plataforma de Machine Learning para construção, treinamento e implantação de modelos.
- **Python:** Linguagem de programação utilizada para manipulação de dados e automação de tarefas.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests com melhorias.

## Licença

Este projeto está licenciado sob a MIT License. Consulte o arquivo LICENSE para obter mais detalhes.
