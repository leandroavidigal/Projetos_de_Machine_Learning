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

## Instruções de Instalação

Siga as instruções abaixo para clonar o repositório e configurar o ambiente de desenvolvimento.

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/loan-approval-prediction.git

2. Navegue até o diretório do projeto:
   ```bash
   cd loan-approval-prediction

3. Crie um ambiente virtual (opcional, mas recomendado):
   ```bash
   python -m venv .venv

4. Ative o ambiente virtual: No Windows:
   ```bash
   .venv\Scripts\activate

No macOS/Linux:
   ``bash
   source .venv/bin/activate

5. Instale as dependências necessárias:
   ```bash
   pip install -r requirements.txt

6. Abra o notebook Jupyter:
   ```bash
   jupyter notebook

7. Abra o arquivo loan_approval_project.ipynb e execute as células passo a passo para reproduzir o projeto.

## Uso
Carregue os dados: O arquivo LoanData.csv será utilizado para carregar o dataset no notebook.
Siga as etapas descritas no notebook para realizar a análise exploratória, tratamento de valores nulos, balanceamento de classes e transformação de variáveis.
O modelo é treinado usando o Random Forest Classifier e o desempenho é avaliado com a métrica de acurácia, além de um relatório de classificação e matriz de confusão.
O modelo final é salvo como loan_approval_model.pkl e pode ser utilizado para previsões futuras.
O arquivo loan_test_data.csv contém os dados de teste para verificar o desempenho em um conjunto separado.

##Resultados
Acurácia do modelo: 82% no conjunto de teste.
O modelo é balanceado usando a técnica SMOTE para lidar com o desbalanceamento de classes.
Utilizamos validação cruzada para garantir a robustez do modelo, obtendo uma acurácia média de 79% com 5-fold cross-validation.
Deploy
Este modelo pode ser integrado em uma aplicação web para previsões em tempo real. A parte 2 deste projeto (a ser adicionada) envolverá a construção de uma interface utilizando Streamlit ou Flask para permitir que usuários finais façam previsões diretamente inserindo seus dados.

##Contribuindo
Se você deseja contribuir para este projeto, sinta-se à vontade para abrir uma issue ou enviar um pull request com melhorias, sugestões de novos recursos ou correções de bugs.

##Licença
Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
