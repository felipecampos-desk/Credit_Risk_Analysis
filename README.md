# 📊 Análise de Risco de Crédito

## Visão Geral

Este projeto tem como objetivo analisar o risco de inadimplência de clientes de cartão de crédito, utilizando técnicas de **Análise Exploratória de Dados (EDA)** e **Teste de Hipótese**.

A proposta simula o papel de um analista de dados em contexto de risco, buscando gerar **insights acionáveis para tomada de decisão**.

---

## Objetivo

Investigar se clientes com histórico de atraso superior a dois meses apresentam **maior probabilidade de inadimplência no mês seguinte**, validando essa hipótese por meio de análise estatística.

---

## Contexto de Negócio

Instituições financeiras enfrentam o desafio de equilibrar:

- Expansão do crédito  
- Controle do risco de inadimplência  

Nesse cenário, compreender o comportamento de pagamento dos clientes é essencial para:

- reduzir perdas financeiras  
- melhorar estratégias de concessão de crédito  
- segmentar clientes por nível de risco  

---

## Dataset Utilizado

Por se tratar de um dado diponível publicamente, segue algumas infomações:
- **Nome:** Default of Credit Card Clients  
- **Fonte:** UCI Machine Learning Repository  

O dataset contém informações sobre:

- limites de crédito  
- histórico de pagamento  
- valores de fatura  
- valores pagos  
- variável alvo: **inadimplência no mês seguinte**

---

## Metodologia

### Análise Exploratória de Dados (EDA)

- Análise univariada das variáveis  
- Identificação de outliers  
- Visualização de distribuições  
- Aplicação de escala logarítmica para melhor interpretação de dados financeiros  

---

### Engenharia de Variáveis

Criação da variável:

- `max_delay`: maior atraso histórico do cliente  

Segmentação de grupos:

- clientes com atraso **≤ 2 meses**  
- clientes com atraso **> 2 meses**

---

### Análise Bivariada

- Relação entre atraso e inadimplência  
- Comparação de grupos de risco  

---

### Teste de Hipótese

Aplicação do:

- **Teste Z para proporções (duas amostras independentes)**  

Hipóteses:

- **H0:** não há diferença entre os grupos  
- **H1:** clientes com atraso >2 meses possuem maior risco  

---

## Principais Resultados

- Taxa de inadimplência para o grupo (≤ 2 meses): **20,43%**  
- Taxa de inadimplência para o grupo (> 2 meses): **62,87%**  
- Diferença: **+42,44 p.p.** (pontos percentuais) 
- Resultado estatisticamente significativo (p-valor ≈ 0), ou seja, **extretamente baixo.**

---

## Insights

- O histórico de atraso é um **forte indicador de risco de crédito**  
- Existe uma **relação clara entre atraso e inadimplência**  
- A análise revelou também:
  - alta dispersão nos valores de fatura  
  - presença de outliers relevantes  
  - leve tendência de aumento nas faturas mais recentes  

---

## Recomendações

- Classificar clientes por nível de risco com base no histórico de atraso  
- Monitorar clientes com sinais iniciais de atraso  
- Aplicar políticas de crédito mais restritivas para clientes de alto risco