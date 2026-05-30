# Projeto Varejo - Análise Exploratória de Dados (AED) aplicada ao varejo.

Projeto irá desenvolver uma análise exploratoria de dados, de registros reais de compras. 
___

## Objetivo:

Preparar uma base para análises mais avançadas ou para alimentar um dashboard. Identificar problemas nos dados, tratar esses problemas com ferramentas adequadas e gerar estatísticas  e funções de agrupamento, para responder perguntas operacionais como:
* Quem compra mais?
* Quais categorias vendem mais?
* Como variam as vendas ao longo do tempo?
___

## Base de Dados:

O projeto utiliza a seguinte base de dados:
* base_varejo_csv: Informações de Vendas do Varejo.

A base de dados inicial apresenta:
Registros/Linhas: 830000 
Colunas:          14

Duplicatas totais: 96553
Total de nulos: 3320000

Insights: 
* 4 colunas estão sem nenhum dado → Serão ser removidas;
* Existem dados duplicados → Serão excluídos, mantendo o registro mais recente;
* Algumas colunas apresentam tipos de dados incompatíveis com seus conteúdos → Devem ser transformadas para o tipo correto.
* Não foram encontradas categorias vazias.

#### Verificação dos tipos de dados:

DATA           str → Transformar em datetime.
CO_ID        int64 → OK
CL_ID        int64 → OK
CL_GENERO      str → OK
CL_EC        int64 → OK
CL_FHL       int64 → OK
CL_SEG         str → OK
PR_ID        int64 → OK
PR_CAT         str → OK
PR_NOME        str → OK
dtype: object

## Tratamento dos Dados:

* 4 colunas vazias removidas;
* Duplicados removidos mantendo o registro mais recente;
* Transformação coluna  'DATA' para datetime;


A base de dados atual apresenta:
Registros/Linhas: 733447 
Colunas:          10

Duplicatas totais: 0
Total de nulos: 0
