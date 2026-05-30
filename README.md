# Projeto Varejo - Análise Exploratória de Dados (AED)

Projeto que desenvolve uma análise exploratória de dados de registros reais de compras do varejo.

---

## Objetivo

Preparar uma base para análises mais avançadas ou para alimentar um dashboard. Identificar problemas nos dados, tratar esses problemas com ferramentas adequadas e gerar estatísticas e funções de agrupamento, para responder perguntas operacionais como:

- Quem compra mais?
- Quais categorias vendem mais?
- Como variam as vendas ao longo do tempo?

---

## Base de Dados

- **Fonte:** base_varejo.csv — Informações de Vendas do Varejo

**Diagnóstico inicial:**

| Métrica | Valor |
|---------|-------|
| Registros/Linhas | 830.000 |
| Colunas | 14 |
| Duplicatas | 96.553 |
| Nulos | 3.320.000 |

**Observações:**
- 4 colunas estão sem nenhum dado → serão removidas
- Existem dados duplicados → serão excluídos, mantendo o registro mais recente
- Algumas colunas apresentam tipos incompatíveis → serão convertidas
- Não foram encontradas categorias vazias em PR_CAT

**Verificação dos tipos de dados:**

| Coluna | Tipo Atual | Status |
|--------|-----------|--------|
| DATA | str | → Converter para datetime |
| CO_ID | int64 | ✅ OK |
| CL_ID | int64 | ✅ OK |
| CL_GENERO | str | ✅ OK |
| CL_EC | int64 | ✅ OK |
| CL_FHL | int64 | ✅ OK |
| CL_SEG | str | ✅ OK |
| PR_ID | int64 | ✅ OK |
| PR_CAT | str | ✅ OK |
| PR_NOME | str | ✅ OK |

---

## Tratamento dos Dados

- 4 colunas vazias removidas
- Verificação de categorias vazias em PR_CAT: nenhum valor nulo encontrado, substituição por "Sem Categoria" não foi necessária
- Duplicatas removidas mantendo o registro mais recente
- Coluna DATA convertida de str para datetime

**Base após limpeza:**

| Métrica | Valor |
|---------|-------|
| Registros/Linhas | 733.447 |
| Colunas | 10 |
| Duplicatas | 0 |
| Nulos | 0 |