# Projeto de Análise Preditiva de Risco de Crédito — FinTech Express

Este repositório contém o projeto de inteligência de dados voltado para a análise e classificação de risco na concessão de crédito pessoal e microcrédito digital na empresa fictícia **FinTech Express Soluções Financeiras Ltda.**.

---

## 📌 Visão Geral do Projeto

O objetivo principal deste projeto é desenvolver um pipeline preditivo de Machine Learning para avaliar o risco de inadimplência de tomadores de crédito, otimizando o processo de aprovação de empréstimos sem aumentar a exposição do portfólio a ativos de alto risco.

* **Organização:** FinTech Express Soluções Financeiras Ltda.
* **Setor:** Serviços Financeiros e Tecnologia (*Fintech*).
* **Alvo de Negócio:** Redução da taxa de inadimplência e identificação precisa do perfil dos clientes.
* **Membro do Projeto:** Rafael Tapigliani Rodrigues (RA: 10441243)

---

## 📊 Estrutura e Dicionário de Dados (Metadados)

Os dados estão armazenados no diretório `data/raw/` e compreendem atributos socioeconômicos e de histórico financeiro:

| Nome do Campo | Tipo de Dado | Descrição do Metadado | Aplicação no Projeto |
| :--- | :--- | :--- | :--- |
| `id_cliente` | String (UUID) | Identificador único e anonimizado do cliente. | Agrupamento de dados por entidade. |
| `idade` | Inteiro | Idade do tomador de crédito (em anos). | Análise demográfica e regressão de risco. |
| `renda_mensal` | Decimal (BRL) | Renda líquida mensal comprovada do cliente. | Avaliação da capacidade de pagamento. |
| `score_credito` | Inteiro (300-850) | Pontuação de crédito do cliente no mercado. | Classificação inicial do perfil de crédito. |
| `vlr_emprestimo` | Decimal (BRL) | Valor total do empréstimo solicitado. | Variável-alvo para modelos orçamentários. |
| `num_parcelas` | Inteiro | Quantidade total de parcelas contratadas. | Cálculo de tempo de exposição ao risco. |
| `historico_inad` | Booleano | Registro prévio de atrasos (0 = Não, 1 = Sim). | Treinamento de modelos preditivos. |
| `status_emprestimo` | Categoria | Situação atual (`Quitado`, `Em Dia`, `Inadimplente`). | Variável dependente/alvo da modelagem. |

---

## 🛠️ Estrutura do Repositório

```text
├── data/
│   ├── raw/            <- Base de dados original (Metadados)
│   └── processed/      <- Dados limpos e preparados
├── docs/               <- Documentação técnica e relatórios do projeto (A1)
├── notebooks/          <- Notebooks Jupyter (.ipynb) contendo análises e modelos
├── README.md           <- Apresentação e instruções do projeto
└── requirements.txt    <- Dependências e bibliotecas Python

---

## 🔬 Metodologia Analítica (Etapa A2)

### 1. Linguagem e Bibliotecas
* **Linguagem:** Python 3.10+
* **Principais Pacotes:** `pandas`, `numpy` (Manipulação); `matplotlib`, `seaborn` (EDA); `scikit-learn` (Modelagem e Métricas).

### 2. Pipeline de Pré-processamento e Modelagem
* **Tratamento de Dados:** Imputação de nulos via mediana, escalonamento via `StandardScaler` e codificação de variáveis categóricas.
* **Modelos Escolhidos:**
  * **Baseline:** Regressão Logística (Alta interpretabilidade e auditoria financeira).
  * **Avançado:** Random Forest Classifier (Captura de não-linearidades e interações).
* **Métricas de Sucesso:**
  * **Acurácia Global:** $> 85\%$
  * **Recall (Inadimplentes):** $\ge 80\%$ (Foco em minimizar Falsos Negativos/prejuízo financeiro).
