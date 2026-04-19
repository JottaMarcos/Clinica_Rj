# 🏥 Clínica RJ — Painel Executivo de Saúde

> Dashboard executivo completo para gestão clínica, integrando análise financeira, eficiência operacional e logística de atendimento.

[![SQL](https://img.shields.io/badge/SQL-PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=flat-square&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-222222?style=flat-square&logo=github&logoColor=white)](https://jottamarcos.github.io/Clinica_Rj)

---

## 📊 Visão Geral

Este projeto consolida **30.000 registros** de atendimentos clínicos (Jan/2025 – Fev/2026) em um painel executivo interativo, permitindo tomada de decisão baseada em dados nas áreas financeira, operacional e logística.

**Acesse o dashboard:** [jottamarcos.github.io/Clinica_Rj](https://jottamarcos.github.io/Clinica_Rj)

---

## 🚀 Stack Tecnológica

| Camada | Tecnologia | Finalidade |
|--------|-----------|------------|
| Extração & Modelagem | **SQL** | Queries de agregação, joins e criação de métricas derivadas |
| Transformação & Análise | **Python** (Pandas, NumPy) | Limpeza de dados, cálculo de KPIs e exportação |
| Visualização BI | **Power BI** | Dashboards interativos com filtros dinâmicos |
| Publicação Web | **HTML/CSS/JS + Chart.js** | Dashboard responsivo hospedado no GitHub Pages |

---

## 💡 Principais Insights Extraídos

### 🔴 Alerta Crítico — Cancelamentos Sistêmicos
> Taxa de cancelamento de **10% uniforme** em todos os planos (Amil, Bradesco Saúde, Hapvida e NotreDame).

A uniformidade entre convênios indica que o problema **não é do plano** — é de processo interno. A ausência de confirmação ativa de consultas resulta em **R$ 965.570 de receita perdida**, equivalente a quase **10% da receita total** de R$ 9,74 Mi.

**Ação recomendada:** Implementar confirmação automática via WhatsApp/SMS 24h antes do agendamento.

---

### 📉 Tendência de Queda no Faturamento
O faturamento caiu de **R$ 271,61 Mil** (pico em mar/2025) para **R$ 233,42 Mil** (fev/2026) — uma retração de **~14% em 12 meses**.

**Hipóteses a investigar:** saída de profissionais, perda de credenciamento em convênios ou sazonalidade não gerenciada.

---

### 💳 Mix de Pagamentos — Oportunidade PIX
| Meio de Pagamento | Participação |
|------------------|-------------|
| PIX | 40,19% |
| Cartão de Crédito | 33,36% |
| Cartão de Débito | 26,46% |

PIX já é o meio dominante. Criar uma **política de desconto exclusivo PIX** pode aumentar ainda mais sua adoção e reduzir custos com taxas de cartão.

---

### 📍 Distribuição Geográfica — Nova Iguaçu como Hub
Nova Iguaçu lidera o volume de atendimentos com **3.172 registros**, superando o próprio município do Rio de Janeiro (3.040). Isso aponta para **demanda reprimida na região** e uma oportunidade de expansão antes que concorrentes percebam.

---

### 🏆 Performance por Plano
| Plano | Receita | Agendamentos | Cancelamento |
|-------|---------|-------------|-------------|
| Amil | R$ 1.517.692,82 | 4.662 | 10% |
| Bradesco Saúde | R$ 1.426.030,33 | 4.415 | 10% |
| Hapvida | R$ 1.401.064,24 | 4.325 | 10% |
| NotreDame | R$ 1.300.730,71 | 4.010 | 10% |

---

### 💊 Ranking de Remédios por Receita
| Categoria | Receita |
|-----------|---------|
| Anti-hipertensivo | R$ 1.298.872,95 |
| Antibiótico | R$ 996.436,53 |
| Anti-inflamatório | R$ 961.529,73 |
| Analgésico | R$ 652.103,80 |

Anti-hipertensivos lideram com folga — garantir estoque estratégico dessa categoria é prioridade.

---

## 📁 Estrutura do Repositório

```
Clinica_Rj/
│
├── index.html              # Dashboard executivo (GitHub Pages)
├── README.md               # Documentação do projeto
│
├── sql/
│   ├── queries.sql         # Queries principais de agregação
│   └── views.sql           # Views criadas para o Power BI
│
├── python/
│   ├── etl.py              # Pipeline de extração e transformação
│   ├── kpis.py             # Cálculo de métricas e KPIs
│   └── requirements.txt    # Dependências Python
│
└── powerbi/
    └── clinica_rj.pbix     # Arquivo Power BI
```

---

## ⚙️ Como Reproduzir

### Pré-requisitos
```bash
Python 3.11+
Power BI Desktop
Banco de dados PostgreSQL (ou adaptar para SQLite)
```

### Instalação
```bash
# Clone o repositório
git clone https://github.com/JottaMarcos/Clinica_Rj.git
cd Clinica_Rj

# Instale as dependências Python
pip install -r python/requirements.txt

# Execute o pipeline ETL
python python/etl.py

# Execute o cálculo de KPIs
python python/kpis.py
```

### Visualização Web
Abra o arquivo `index.html` diretamente no navegador ou acesse via [GitHub Pages](https://jottamarcos.github.io/Clinica_Rj).

---

## 📈 KPIs Monitorados

**Financeiro**
- Receita Total | Receita Líquida | Receita Perdida
- Ticket Médio por Consulta
- Taxa de Cancelamento por Plano
- Mix de Meios de Pagamento

**Operacional**
- Consultas Realizadas vs Agendadas por Mês
- Performance Individual por Médico (CRM, Turno, Especialidade)
- Taxa de Ocupação da Clínica por Hora
- Mix Presencial vs Telemedicina

**Logística**
- Distribuição Geográfica de Atendimentos
- Ranking de Remédios por Categoria e Receita
- Status de Estoque
- Ranking Regional (Top 7 Estados)

---

## 🗂️ Fonte dos Dados

Dados sintéticos gerados para fins educacionais e de portfólio, simulando o ambiente operacional de uma rede de clínicas do Rio de Janeiro com múltiplos convênios, especialidades e unidades regionais.

---

## 👤 Autor

**João Marcos**
- GitHub: [@JottaMarcos](https://github.com/JottaMarcos)

---

<p align="center">Feito com SQL, Python e Power BI</p>
