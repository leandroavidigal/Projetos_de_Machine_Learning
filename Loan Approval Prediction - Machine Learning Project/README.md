# Loan Approval Prediction - Machine Learning Project

## Descrição do Projeto

Este é um projeto completo de machine learning com o objetivo de prever a aprovação de empréstimos com base em características pessoais e financeiras dos solicitantes. O modelo foi desenvolvido para aprender padrões e relações entre variáveis, como renda do solicitante, histórico de crédito e status de casamento, para prever se o empréstimo será aprovado. Este repositório inclui todas as etapas do projeto, desde a coleta e preparação dos dados até o treinamento e avaliação do modelo, além de preparar o modelo para deploy.

## Objetivo do Projeto

O objetivo é construir um modelo que possa prever se um solicitante terá seu empréstimo aprovado ou não. Isso ajuda instituições financeiras a tomarem decisões de crédito mais rápidas e eficazes.

## Conjunto de Dados

O conjunto de dados utilizado contém informações de vários solicitantes e inclui as seguintes variáveis:

- **Loan_ID**: Identificação única de cada solicitação de empréstimo
- **Gender**: Gênero do solicitante
- **Married**: Status de casamento do solicitante
- **Dependents**: Número de dependentes do solicitante
- **Education**: Nível de escolaridade
- **Self_Employed**: Indica se o solicitante é autônomo
- **ApplicantIncome**: Renda mensal do solicitante
- **CoapplicantIncome**: Renda mensal do co-solicitante, se houver
- **LoanAmount**: Valor solicitado de empréstimo
- **Loan_Amount_Term**: Prazo do empréstimo em meses
- **Credit_History**: Histórico de crédito
- **Property_Area**: Localização do imóvel
- **Loan_Status**: Status de aprovação do empréstimo (variável alvo)

O dataset utilizado está disponível no arquivo **LoanData.csv** incluído neste repositório.

## Estrutura do Projeto

- **loan_approval_project.ipynb**: Notebook Jupyter com todas as etapas do projeto.
- **LoanData.csv**: Conjunto de dados utilizado para treinar o modelo.
- **loan_approval_model.pkl**: Modelo treinado salvo para deploy.
- **loan_test_data.csv**: Dados de teste utilizados na avaliação do modelo.

## Tecnologias Utilizadas

- **Python 3.9**
- **Pandas** - Para manipulação de dados.
- **NumPy** - Para cálculos matemáticos.
- **Matplotlib & Seaborn** - Para visualização de dados.
- **Scikit-learn** - Para pré-processamento, modelagem e avaliação.
- **Imbalanced-learn** - Para balanceamento de classes com SMOTE.
- **Joblib** - Para salvar o modelo treinado.
- **Jupyter Notebook** - Para desenvolvimento interativo.


