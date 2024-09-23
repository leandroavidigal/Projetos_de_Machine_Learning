# Projetos de Machine Learning

Bem-vindo ao repositório **Projetos de Machine Learning**, onde são explorados diferentes projetos práticos, aplicando técnicas e algoritmos de aprendizado de máquina para resolver problemas reais. Cada projeto apresenta desde o processamento de dados até o desenvolvimento, avaliação de modelos e, quando aplicável, a implementação para deploy.

## Objetivo do Repositório
Este repositório foi criado com o objetivo de compartilhar conhecimento e demonstrar minha experiência em Machine Learning e ciência de dados. Cada projeto aborda desafios específicos, desde classificação até previsão, utilizando diversas ferramentas e abordagens modernas. Aqui você encontrará a aplicação de técnicas de modelagem, pré-processamento de dados, validação cruzada, e métricas de avaliação.

## Projetos

### 1. **Loan Approval Prediction - Machine Learning Project**
**Descrição:**  
Este projeto tem como objetivo prever a aprovação de empréstimos com base em características pessoais e financeiras dos solicitantes, como renda, histórico de crédito, e status de casamento. O modelo foi treinado e avaliado utilizando diversas métricas de desempenho, e foi preparado para implementação em um ambiente de produção.

**Objetivo:**  
Auxiliar instituições financeiras a tomar decisões rápidas e eficazes em relação à aprovação de crédito.

**Principais etapas:**
- Coleta e preparação de dados
- Desenvolvimento de modelos de machine learning
- Avaliação de métricas (precisão, recall, F1-score)
- Implementação para deploy

---

### 2. **Previsão de Estoque usando Amazon SageMaker**
**Descrição:**  
Neste projeto, foi desenvolvido um modelo de previsão de estoque utilizando o Amazon SageMaker. O objetivo é prever a demanda futura com base em variáveis como promoções e datas de eventos. A implementação incluiu a criação de um pipeline completo, desde a seleção do dataset até a análise e previsão dos resultados.

**Principais etapas:**
- Seleção e preparação do dataset
- Treinamento do modelo no SageMaker
- Avaliação de métricas como wQL, MAPE, RMSE, WAPE, e MASE
- Implementação de previsões automáticas de estoque

**Resultados:**  
As métricas de desempenho mostraram que o modelo tem uma precisão razoável para as previsões de estoque, com algumas oportunidades de otimização para melhorar a acurácia.

---

### 3. **Classificação de Câncer Baseada em Expressões Genéticas**
**Descrição:**  
Este projeto visa classificar dois tipos de câncer (Leucemia Linfoblástica Aguda e Leucemia Mieloide Aguda) utilizando dados de expressão genética. Modelos de Regressão Logística e Principal Component Regression (PCR) foram implementados para avaliar a precisão preditiva e o impacto da redução de dimensionalidade por PCA.

**Principais etapas:**
- Exploração e normalização dos dados genéticos
- Desenvolvimento de modelos de Regressão Logística e PCR
- Aplicação de PCA para redução de dimensionalidade
- Validação cruzada dos modelos

**Resultados:**  
A redução de dimensionalidade impactou positivamente a capacidade preditiva dos modelos, com o PCR superando a Regressão Logística em termos de precisão.

## Configuração e Ferramentas
Todos os projetos utilizam as seguintes bibliotecas e ferramentas:

- **Python 3.8+**
- **NumPy** e **pandas** para manipulação de dados
- **scikit-learn** para modelagem e avaliação de modelos
- **Matplotlib** e **Seaborn** para visualização de dados
- **Jupyter Notebook** para desenvolvimento e análise interativa
- **Amazon SageMaker** para execução de modelos em escala
- **PCA** para redução de dimensionalidade

## Como Contribuir
Se deseja contribuir para este repositório, siga os passos abaixo:

1. Faça o fork do projeto.
2. Crie uma branch para suas alterações: `git checkout -b minha-branch`.
3. Faça suas modificações.
4. Envie suas alterações: `git push origin minha-branch`.
5. Abra um Pull Request.
