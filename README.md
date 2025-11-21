# 📊 Análise da Inadimplência no Brasil

Este projeto analisa a evolução da inadimplência no Brasil e sua relação com crédito total, Selic e inflação (IPCA e IPCA 12 meses), utilizando séries temporais do Banco Central (SGS). O objetivo é entender padrões, identificar ciclos e construir um modelo de regressão capaz de prever a inadimplência.

---

## 📁 Variáveis utilizadas
- **Inadimplência (%)** — SGS 21082  
- **Crédito Total (R$ mi)** — SGS 20786  
- **Selic (%)** — SGS 4189  
- **IPCA (%)** — SGS 433  
- **IPCA 12 meses** — calculado via soma móvel  

---

## 🔍 Principais análises
- Evolução temporal de cada uma das variáveis  
- Analise bivariada entre inadimplência e crédito total (normalizado para leitura visual)  
- Analise bivariada entre inadimplência e IPCA 12 meses
- Analise bivariada entre inadimplência e Selic   
- Identificação de ciclos e mudanças de direção  
- Análises gráficas com foco em comportamento e tendência  

---

## 🤖 Modelagem
Foi utilizado o XGBoost Regressor

A divisão treino–teste respeitou a ordem temporal (últimos 20% dos dados separados para teste).

### 📈 Resultados
O modelo apresentou o seguinte desempenho:

- **RMSE:** 0.1151  
- **MAE:** 0.0876  

Esses valores indicam que o modelo consegue acompanhar bem as oscilações da série e reproduz principalmente as **mudanças de tendência**, que são essenciais para previsões macroeconômicas.

---

## 📝 Conclusões
- A inadimplência apresenta ciclos claros ao longo do tempo, com quedas e altas bem definidas.  
- O **XGBoost** se mostrou adequado para capturar a dinâmica da série, com erros baixos e boa capacidade de previsão.  
