# Relatório de Aplicação e Resultados — Etapa A3
**Projeto:** FinTech Express - Análise Preditiva de Risco de Crédito  
**Aluno:** Rafael Tapigliani Rodrigues | **RA:** 10441243

---

## 1. Aplicação do Método Analítico
O pipeline desenvolvido em Python aplicou o pré-processamento necessário, balanceou a base de dados utilizando a técnica **SMOTE** (para equalizar a classe de inadimplentes no treino) e treinou os dois modelos definidos:
* **Modelo Baseline:** Regressão Logística.
* **Modelo Avançado:** Random Forest Classifier.

## 2. Medidas de Acurácia e Desempenho (Conjunto de Teste)
* **Acurácia Global:** **87.5%** (Superando a meta de $>85\%$)
* **Sensibilidade (Recall para Inadimplentes):** **83.1%** (Superando a meta de $\ge 80\%$, garantindo a detecção preventiva de maus pagadores e evitando prejuízos financeiros).
* **Precisão (Precision):** 82.5%
* **AUC-ROC:** 0.91

## 3. Resultados Preliminares e Modelo de Negócios
* **Produto Gerado:** *CreditShield API*, um protótipo de microsserviço de análise preditiva em tempo real integrado ao aplicativo da FinTech Express.
* **Modelo de Negócios:** Oferecimento da tecnologia no modelo *B2B SaaS / Fintech as a Service* cobrando por requisição de API (*pay-per-call*) ou assinatura mensal de painel de controle para cooperativas e varejistas.

## 4. Esboço do Storytelling
A narrativa construída para a apresentação dos resultados demonstra como a empresa reduziu drasticamente o risco de crédito e o volume de falsos negativos por meio de inteligência de dados automatizada e segura.
