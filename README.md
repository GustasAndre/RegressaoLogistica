
# #Projeto de Regressão Logística: Análise de Modelagem de Empréstimos Pessoais

Este repositório contém um código em Python que realiza a modelagem de dados de um conjunto de dados de empréstimos pessoais. O objetivo é prever se um cliente aceitará um empréstimo pessoal com base em diversas características.

## Estrutura do Código

O código utiliza as seguintes bibliotecas:
- `pandas`: Para manipulação de dados.
- `scikit-learn`: Para divisão dos dados, modelagem e avaliação de métricas.
- `matplotlib` e `seaborn`: Para visualização de dados.

## Conjunto de Dados

O conjunto de dados utilizado está disponível em `Bank_Personal_Loan_Modelling.xlsx`, que contém as seguintes colunas relevantes:

- **Age**: Idade do cliente.
- **Experience**: Anos de experiência do cliente.
- **Income**: Renda do cliente.
- **Family**: Número de membros da família.
- **CCAvg**: Média de gastos em cartões de crédito.
- **Education**: Nível educacional do cliente.
- **Mortgage**: Valor da hipoteca.
- **Securities_Account**: Indica se o cliente possui conta em títulos.
- **CD_Account**: Indica se o cliente possui conta em certificados de depósito.
- **Online**: Indica se o cliente utiliza serviços online.
- **CreditCard**: Indica se o cliente possui cartão de crédito.
- **Personal_Loan**: Variável alvo (1 se o cliente aceitou o empréstimo, 0 caso contrário).

## Passos Realizados

1. **Leitura do Conjunto de Dados**:
   ```python
   df = pd.read_excel("/content/Bank_Personal_Loan_Modelling.xlsx")

2. Análise Exploratória:
  Exibição dos tipos de dados.
  Estatísticas descritivas.
  Verificação de valores ausentes.
  Remoção da coluna ID.

3. Divisão dos Dados:
  Divisão dos dados em conjuntos de treino e teste (80% treino, 20% teste).

4.Treinamento do Modelo:
  Utilização de Logistic Regression para modelagem.
  model = LogisticRegression()
  model.fit(X_train, y_train)

Predições:

Predição utilizando o conjunto de teste.
Matriz de Confusão:

Visualização da matriz de confusão:

![Matriz de Confusão](https://github.com/GustasAndre/RegressaoLogistica/blob/c84592db073dc12eb61f0eb012337a8a6017f280/Matriz%20de%20confus%C3%A3o.png)

Métricas de Avaliação:

Acurácia:

Acurácia Teste: accuracy_score(y_test, y_pred)

Acurácia Treino: accuracy_score(y_train, model.predict(X_train))

Acurácia Balanceada:

Acurácia Balanceada Teste: balanced_accuracy_score(y_test, y_pred)

Acurácia Balanceada Treino: balanced_accuracy_score(y_train, model.predict(X_train))

Precisão:

Precisão Teste: precision_score(y_test, y_pred)

Precisão Treino: precision_score(y_train, model.predict(X_train))

Recall:

Recall Teste: recall_score(y_test, y_pred)

Recall Treino: recall_score(y_train, model.predict(X_train))

F1 Score:

F1 Score Teste: f1_score(y_test, y_pred)

F1 Score Treino: f1_score(y_train, model.predict(X_train))

Curva ROC:

Visualização da curva ROC:

![Curva ROC](https://github.com/GustasAndre/RegressaoLogistica/blob/c84592db073dc12eb61f0eb012337a8a6017f280/Curva%20Roc.png)


Conclusão

Este código fornece uma análise detalhada sobre a modelagem de empréstimos pessoais, incluindo a avaliação do desempenho do modelo através de métricas como precisão, recall e F1 Score. As visualizações ajudam a entender melhor a eficácia do modelo.

Como Executar
Para executar o código, você precisa ter as bibliotecas mencionadas instaladas. Você pode instalar as dependências usando:
  pip install pandas scikit-learn matplotlib seaborn openpyxl
