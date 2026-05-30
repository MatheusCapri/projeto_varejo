# Projeto Varejo - Análise Exploratória de Dados (AED) aplicada ao varejo.

<<<<<<< HEAD
Projeto deve desenvolver uma análise exploratoria de dados, de registros reais de compras. 
=======
Projeto irá desenvolver uma análise exploratoria de dados, de registros reais de compras. 
>>>>>>> 1661978af8f7fac91e239e85242b7d07048e5f14
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

<<<<<<< HEAD
=======
A base de dados inicial apresenta:

Registros/Linhas: 830000 
Colunas:          14
>>>>>>> 1661978af8f7fac91e239e85242b7d07048e5f14


A base de dados inicial apresenta:
Registros/Linhas:    830000 

Colunas:             14


Duplicatas totais:   96553

Total de nulos:      3320000


Observações: 
* 4 colunas estão sem nenhum dado → Serão ser removidas;
* Existem dados duplicados → Serão excluídos, mantendo o registro mais recente;
* Algumas colunas apresentam tipos de dados incompatíveis com seus conteúdos → Devem ser transformadas para o tipo correto.
* Não foram encontradas categorias vazias.



#### Verificação dos tipos de dados:

| Coluna    | Tipo Atual | Status |
|-----------|------------|--------|
| DATA      |    str     | → Converter para datetime |
| CO_ID     |    int64   | ✅ OK |
| CL_ID     |    int64   | ✅ OK |
| CL_GENERO |    str     | ✅ OK |
| CL_EC     |    int64   | ✅ OK |
| CL_FHL    |    int64   | ✅ OK |
| CL_SEG    |    str     | ✅ OK |
| PR_ID     |    int64   | ✅ OK |
| PR_CAT    |    str     | ✅ OK |
| PR_NOME   |    str     | ✅ OK |


## Tratamento dos Dados:

* 4 colunas vazias removidas;
* Realizada a verificação de categorias vazias em PR_CAT, nenhum valor nulo foi encontrado, por isso não foi substituido por 'Sem Categoria";
* Duplicados removidos mantendo o registro mais recente;
* Transformação coluna  'DATA' para datetime;

A base de dados atual (após limpeza) apresenta:
Registros/Linhas:   733447 
Colunas:            10

<<<<<<< HEAD
Duplicatas totais:  0
Total de nulos:     0
=======
A base de dados atual apresenta:
Registros/Linhas: 733447 
Colunas:          10

Duplicatas totais: 0
Total de nulos: 0
>>>>>>> 1661978af8f7fac91e239e85242b7d07048e5f14
