# 🛡️ FinTech Express — Análise Preditiva de Risco de Crédito

Projeto desenvolvido para a avaliação das etapas **A1, A2 e A3** do componente curricular de Ciência de Dados.

## 📌 1. Visão Geral do Projeto (A1)
* **Organização:** FinTech Express Soluções Financeiras Ltda.
* **Setor:** Serviços Financeiros e Tecnologia (*Fintech*).
* **Objetivo:** Desenvolver um pipeline preditivo em Python para classificação de risco de crédito e prevenção à inadimplência.
* **Aluno:** Rafael Tapigliani Rodrigues | **RA:** 10441243

---

## 📊 2. Metadados e Base de Dados
A base tabular encontra-se em `data/raw/dataset.csv` e possui a seguinte estrutura:
* `id_cliente`: Identificador único (UUID).
* `idade`: Idade do cliente em anos.
* `renda_mensal`: Renda mensal comprovada (BRL).
* `score_credito`: Pontuação de crédito (300 a 850).
* `vlr_emprestimo`: Valor solicitado (BRL).
* `num_parcelas`: Duração do contrato em meses.
* `historico_inad`: Registro prévio de atrasos (0 = Não, 1 = Sim).
* `status_emprestimo`: Classe Alvo (`Quitado`, `Em Dia`, `Inadimplente`).

---

## 🔬 3. Metodologia Analítica (A2)
* **Linguagem:** Python 3.10+
* **Estratégia:** Limpeza de dados, codificação categórica, padronização via `StandardScaler` e balanceamento via `SMOTE`.
* **Modelos:** 
  * *Baseline:* Regressão Logística.
  * *Avançado:* Random Forest Classifier.

---

## 📈 4. Resultados e Métricas (A3)
* **Acurácia Global:** **87.5%** (Meta: $>85.0\%$)
* **Recall (Inadimplentes):** **83.1%** (Meta: $\ge 80.0\%$)
* **Produto Gerado:** *CreditShield API* — Motor de decisão de risco em tempo real.
* **Modelo de Negócios:** B2B SaaS (*Fintech as a Service*) com cobrança por chamada de API ou assinatura mensal.

---

## 🛠️ Estrutura do Repositório
```text
├── data/
│   └── raw/
│       └── dataset.csv                      <- Base de dados original
├── docs/
│   └── relatorio_A3.md                      <- Relatório de Resultados e Storytelling
├── notebooks/
│   ├── 01_eda_e_preprocessamento.ipynb     <- Análise Exploratória e Limpeza (A2)
│   └── 02_modelagem.ipynb                  <- Treinamento e Avaliação de Métricas (A3)
├── README.md                                <- Documentação principal do repositório
└── requirements.txt                         <- Bibliotecas e dependências Python
