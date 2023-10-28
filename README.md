# Clusterização de clientes de cartão de crédito 💳

Neste projeto, eu utilizei a técnica de **clusterização** para segmentar os clientes de cartão de crédito de um banco, usando o algoritmo **K-Means**.

## Dados 📊

Os dados foram obtidos do arquivo CC GENERAL.csv, que contém as seguintes variáveis:

- **CUST_ID**: identificação do cliente
- **BALANCE**: saldo médio do cliente
- **BALANCE_FREQUENCY**: frequência com que o saldo é atualizado
- **PURCHASES**: valor total das compras
- **ONEOFF_PURCHASES**: valor das compras à vista
- **INSTALLMENTS_PURCHASES**: valor das compras parceladas
- **CASH_ADVANCE**: valor dos saques em dinheiro
- **PURCHASES_FREQUENCY**: frequência das compras
- **ONEOFF_PURCHASES_FREQUENCY**: frequência das compras à vista
- **PURCHASES_INSTALLMENTS_FREQUENCY**: frequência das compras parceladas
- **CASH_ADVANCE_FREQUENCY**: frequência dos saques em dinheiro
- **CASH_ADVANCE_TRX**: número de transações de saques em dinheiro
- **PURCHASES_TRX**: número de transações de compras
- **CREDIT_LIMIT**: limite de crédito do cliente
- **PAYMENTS**: valor total dos pagamentos
- **MINIMUM_PAYMENTS**: valor mínimo dos pagamentos
- **PRC_FULL_PAYMENT**: percentual do saldo pago integralmente
- **TENURE**: tempo de relacionamento com o banco

## Bibliotecas 📚

As bibliotecas utilizadas neste projeto foram:

- **pandas**: para manipular os dados
- **matplotlib**: para gerar gráficos
- **seaborn**: para gerar gráficos estatísticos
- **sklearn**: para realizar a clusterização e a avaliação dos clusters

## Análise 🔎

A análise foi dividida em cinco etapas:

1. Exploração dos dados: nesta etapa, eu verifiquei as características dos dados, como o número de observações, os tipos das variáveis, os valores ausentes.
2. Pré-processamento dos dados: nesta etapa, eu realizei algumas transformações nos dados, como remover a variável CUST_ID, tratar os valores ausentes, padronizar as variáveis numéricas e reduzir a dimensionalidade dos dados usando o PCA.
3. Validação de clusters: nesta etapa, eu utilizei índices para validação dos clusters para o algoritmo K-Means: índice Davies-Bouldin e o calinski harabasz.
4. Nesta etapa, apliquei o algoritmo K-Means com o número ótimo de clusters encontrado na etapa anterior e criei uma nova variável chamada CLUSTER para indicar a qual cluster cada cliente pertence.
5. Análise dos clusters: nesta etapa, eu analisei as características e os perfis dos clientes de cada cluster, usando gráficos e tabelas. Eu também dei nomes aos clusters baseados nas suas principais características.

## Resultados 🏆

Os principais resultados obtidos foram:

- O número ótimo de clusters foi 4.
- Os quatro clusters criados foram nomeados como: 
    - Cluster 0: Clientes com baixo consumo e baixo pagamento (**Low Spenders and Payers**)
    - Cluster 1: Clientes com alto consumo e alto pagamento (**High Spenders and Payers**)
    - Cluster 2: Clientes com alto consumo e baixo pagamento (**High Spenders and Low Payers**)
    - Cluster 3: Clientes com baixo consumo e alto pagamento (**Low Spenders and High Payers**)
- O cluster 0 foi o maior, com 3.717 clientes (61%), seguido pelo cluster 2, com 1.389 clientes (23%), pelo cluster 3, com 603 clientes (10%) e pelo cluster 1, com 292 clientes (5%).
- O cluster 1 foi o que teve os maiores valores médios de saldo, compras, saques, limite de crédito e pagamentos. O cluster 2 foi o que teve os menores valores médios de pagamentos e percentual de pagamento integral. O cluster 3 foi o que teve os menores valores médios de saldo, compras, saques e limite de crédito. O cluster 0 foi o que teve os menores valores médios de frequência de compras e saques.

## Conclusão 🎓

A conclusão deste projeto foi que a técnica de clusterização foi útil para segmentar os clientes de cartão de crédito de um banco, usando o algoritmo K-Means. A análise mostrou que os clientes se dividem em quatro grupos distintos, com diferentes padrões de consumo, pagamento e crédito. Esses grupos podem ser usados para definir estratégias de marketing, fidelização e cobrança para cada segmento de clientes.
