# 📊 Análise de Churn de Clientes - Telecom X

Este repositório contém um projeto completo de Análise de Dados focado em entender e reduzir a evasão de clientes (Churn) de uma empresa fictícia de telecomunicações, a Telecom X. 

O projeto foi desenvolvido inteiramente em **Python** utilizando o **Google Colab**, passando por todas as etapas fundamentais de um projeto de Data Science: desde a coleta e tratamento dos dados (ETL) até a Análise Exploratória (EDA) para extração de insights de negócios.

---

## 🎯 Objetivo do Projeto
A Telecom X vem enfrentando um alto índice de perda de clientes. O objetivo desta análise é investigar a base de dados da empresa Telecom X para identificar padrões de comportamento que levam ao cancelamento do serviço, permitindo que a equipe de negócios crie estratégias de retenção mais eficientes.

## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Linguagem:** Python
* **Ambiente:** Google Colab / Jupyter Notebook
* **Manipulação e Limpeza de Dados:** `pandas`, `numpy`, `json`
* **Visualização de Dados:** `matplotlib`, `seaborn`

## 🗂️ Estrutura dos Dados
Os dados foram extraídos via API em formato JSON aninhado e continham informações demográficas, detalhes da conta e os serviços contratados por cada cliente.
Durante o processo, os dados foram transformados em um formato tabular e as colunas foram traduzidas e padronizadas para facilitar a compreensão.

## ⚙️ Metodologia (Passo a Passo)

1. **Coleta e ETL (Extração, Transformação e Carga):**
   * Leitura dos dados JSON diretamente da API usando a biblioteca `requests`.
   * Achatamento (flattening) de estruturas aninhadas usando `pd.json_normalize`.
   * Limpeza de strings invisíveis e tratamento de valores vazios (NaN).
   * Conversão de tipos de dados (ex: transformando cobranças totais em valores numéricos `float`).
2. **Feature Engineering (Engenharia de Recursos):**
   * Criação da coluna `Cobranca_Diaria` a partir do faturamento mensal para refinar a análise financeira.
   * Tradução do dataset para o Português e binarização da variável alvo `Churn` (0 = Ficou, 1 = Saiu).
3. **Análise Exploratória de Dados (EDA):**
   * Geração de estatísticas descritivas (médias, medianas, contagens).
   * Criação de visualizações (Gráficos de Barras, Gráficos de Pizza e Boxplots) para entender a distribuição do Churn cruzado com variáveis como Tempo de Contrato, Gênero, Método de Pagamento e Valor da Fatura.

## 💡 Principais Insights e Descobertas
* **Taxa de Evasão:** A empresa possui uma taxa de churn alarmante de **26,5%**.
* **O Perigo do Contrato Mensal:** A esmagadora maioria dos clientes que cancelam possuem contrato do tipo "Mensal". Contratos anuais ou bianuais garantem forte retenção.
* **Período Crítico:** Clientes recentes são os mais propensos a sair. A mediana de permanência de quem cancela é de apenas 10 meses.
* **Fator Financeiro e Pagamento:** Faturas mais altas estão correlacionadas com maior taxa de saída. Além disso, clientes que utilizam "Cheque Eletrônico" apresentam uma taxa de evasão desproporcionalmente maior em comparação com pagamentos automáticos.

## 🚀 Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone [git@github.com:neigit485/Challeng-_TelecomX_BR_Evasao_Clientes.git](git@github.com:neigit485/Challeng-_TelecomX_BR_Evasao_Clientes.git)
