# 📊 Análise de Evasão de Clientes - Telecom X

Telecom X - Análise de Evasão de Clientes

**Projeto Churn de Clientes: Entendendo e Combatendo a Evasão**

Introdução

Este relatório detalha as etapas iniciais do projeto "Churn de Clientes" na Telecom X, um esforço crucial para entender e mitigar o alto índice de cancelamentos enfrentado pela empresa. Como assistente de análise de dados, meu papel é coletar, tratar e analisar os dados dos clientes para extrair insights valiosos. Esses insights servirão de base para a equipe de Data Science desenvolver modelos preditivos e estratégias eficazes de retenção.

Objetivo do Projeto: 
O objetivo principal deste projeto é transformar dados brutos em informações estratégicas que ajudem a Telecom X a:

-Identificar os principais fatores que levam os clientes a cancelar seus serviços.

-Prever clientes em risco de churn antes que eles cancelem.

-Desenvolver estratégias proativas para reter clientes valiosos.


## 📁 Conjunto de Dados
**Fonte:** [Seaborn Tips Dataset](https://github.com/mwaskom/seaborn-data/blob/master/tips.csv)  
**Variáveis Relevantes:**
- `Churn`: Indicador de evasão (1 = Evasão, 0 = Ativo)
- `Conta_Total`: Valor total da conta
- `Periodo`: Horário da refeição (Almoço/Jantar)
- `Fumante`: Indicador de clientes fumantes
- `Dia`: Dia da semana

## 🔍 Metodologia

### 1. Preparação dos Dados
```python
# Código de limpeza e transformação
df.drop_duplicates(inplace=True)
df['Contas_Diarias'] = df['Conta_Total'] / 30
mapeamento = {'Male': 1, 'Female': 0, 'Yes': 1, 'No': 0}
df['Sexo'] = df['Sexo'].map(mapeamento)
