[![author](https://img.shields.io/badge/author-rgolino-red.svg)](https://www.linkedin.com/in/renato-golino/) [![](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-365/) [![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/rafaelnduarte/portfolio/issues)


# Projeto de Detecção de Fraude em Cartões de Crédito
<img src ="https://img.freepik.com/fotos-gratis/plano-de-fundo-do-hacker-de-matriz_23-2150082007.jpg?t=st=1732052038~exp=1732055638~hmac=64a55aebfb48f3af448434e6edd92d6c94dab26bbe564c34d673870834de433e&w=1380">

## Objetivo do Projeto

O objetivo principal deste projeto é construir um sistema de aprendizado de máquina capaz de identificar transações fraudulentas em cartões de crédito com alta precisão. O projeto busca explorar um dataset desbalanceado e aplicar técnicas de análise de dados, balanceamento de classes e modelagem preditiva para detectar comportamentos anômalos que caracterizam fraudes financeiras.

## Aplicações
Este tipo de projeto tem aplicações práticas em diversos contextos, incluindo:
- **Bancos e Instituições Financeiras**: Monitoramento em tempo real de transações para prevenir perdas financeiras e proteger clientes.
- **Provedores de Pagamento**: Empresas como PayPal, Stripe e Square podem integrar modelos como este para aumentar a segurança de suas plataformas.
- **Segurança Cibernética**: Análises preventivas de dados transacionais para mitigar riscos de fraudes futuras.
- **Seguradoras**: Detecção de comportamentos fraudulentos em pedidos de indenizações relacionados a cartões de crédito.




## Pipeline do Projeto

### 1. Configuração Inicial
- Instalação de bibliotecas:
  - `scikit-plot`
  - Versão específica do `scipy`.
- Importação de bibliotecas como:
  - `pandas`, `numpy`, `seaborn`, `scikit-learn`, e `imbalanced-learn`.

### 2. Carregamento e Pré-processamento dos Dados
- Importação do dataset de transações.
- Divisão do dataset em:
  - Conjunto de **treino** (85% dos dados).
  - Conjunto de **teste** (15% dos dados).
- Inspeção inicial:
  - Verificação de valores ausentes.
  - Análise do desbalanceamento das classes (fraudes vs. transações normais).

### 3. Análise Exploratória de Dados (EDA)
- **Distribuição de Classes**: Gráficos de barras para análise visual do desbalanceamento.
- **Análise Temporal**: Histogramas da distribuição temporal de fraudes e transações normais.
- **Análise Monetária**: Boxplots para verificar padrões de valores entre fraudes e transações normais.
- **Análise de Variáveis**: KDE plots para comparar distribuições de variáveis entre classes.

### 4. Preparação dos Dados
- Padronização das variáveis contínuas (`Amount` e `Time`) com `StandardScaler`.
- Tratamento do desbalanceamento com `RandomUnderSampler`:
  - Redução das transações normais para equilibrar o número de exemplos.

### 5. Análise de Correlação
- Cálculo da matriz de correlação antes e depois do balanceamento.
- Visualização das correlações com heatmaps.

### 6. Treinamento do Modelo
- Algoritmo utilizado: **Regressão Logística**.
- Conjunto balanceado usado para treinamento.

### 7. Avaliação do Modelo
- Métricas utilizadas:
  - **Relatório de classificação**: Precisão, recall e F1-score.
  - **Curva ROC AUC**: Avaliação visual e métrica quantitativa.
  - **Matriz de Correlação**: Análise do impacto do balanceamento nos dados.

## Como Executar
1. Certifique-se de ter as bibliotecas necessárias instaladas:
   ```bash
   pip install -r requirements.txt
   ```
2. Execute o notebook no ambiente Jupyter ou Colab.

## Observações
- Este projeto utiliza técnicas de balanceamento de classes devido à alta desproporção de transações normais e fraudulentas no dataset.
- Os dados foram obtidos de uma fonte pública (link presente no notebook).

## Resultados
- Um modelo de Regressão Logística foi construído e avaliado, apresentando boa capacidade de diferenciar fraudes de transações legítimas com base nas métricas de avaliação.

- O projeto proporcionou tanbém:
  1. **Modelo Preciso**: Um modelo preditivo que diferencie transações legítimas de fraudulentas com alto grau de acurácia.
  2. **Redução de Falsos Positivos/Negativos**: Otimização das métricas de desempenho para minimizar tanto a classificação errada de transações legítimas quanto a não detecção de fraudes.
  3. **Insights sobre o Dataset**: Melhor compreensão de padrões e anomalias nos dados de transações financeiras.
  4. **Implementação Prática**: Desenvolvimento de um pipeline reutilizável que pode ser adaptado a outros conjuntos de dados ou sistemas de monitoramento em tempo real.

## Projeto Completo

[Fraude Cartão de Crédito](https://github.com/rgolino/Deteccao_Fraude_Cartao_de_Credito/blob/main/PROJETO_Detec%C3%A7%C3%A3o_de_Fraude_em_Cart%C3%B5es_de_Cr%C3%A9dito.ipynb)
