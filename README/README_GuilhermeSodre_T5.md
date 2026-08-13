Mini-Projeto Avaliativo - Análise de Dados com Python

Aluno: Guilherme Sodré  Marques
Turma: Análise de Dados com Python - T5  
Projeto: Mini-Projeto Avaliativo   

Sobre o projeto

Este projeto apresenta uma Análise Exploratória de Dados (AED) aplicada a uma base de dados de varejo.

O objetivo principal foi transformar os dados brutos em uma base mais organizada e confiável, permitindo realizar análises estatísticas e identificar padrões presentes nos dados.

Arquivos do projeto:

- Miniprojeto_GuilhermeSodre_T5.ipynb - Notebook contendo o desenvolvimento e a análise do projeto.
- Miniprojeto_GuilhermeSodre_T5.py - Código Python completo do mini-projeto.
- dataset/Base Varejo.csv - Base de dados original utilizada na análise.
- df_limpo.csv - Base de dados gerada após os tratamentos de limpeza.
- README.md - Documentação completa do projeto.
- README_GuilhermeSodre_T5.md - Instruções para execução do projeto.

Como executar

No Jupyter Notebook / VS Code

1 - Clone ou faça o download deste repositório.

2 - Abra a pasta do projeto no VS Code.

3 - Abra o arquivo Miniprojeto_GuilhermeSodre_T5.ipynb.

4 - Verifique se o arquivo Base Varejo.csv está dentro da pasta dataset.

5 - Execute as células do notebook em ordem, do início ao fim.


Bibliotecas utilizadas

O projeto utiliza:
- Python
- Pandas
- NumPy
- CSV
- IPython Display

realizadas as seguintes etapas para concluir o miniprojeto:

1- Importação da base de dados.
2- Verificação da estrutura e dos tipos de dados.
3- Padronização e transformação de strings.
4- Conversão de dados numéricos e datas.
5- Identificação e tratamento de valores nulos.
6- Tratamento de categorias vazias.
7- Remoção de colunas completamente vazias.
8- Identificação e remoção de registros duplicados.
9- Estatísticas descritivas da quantidade de filhos dos clientes.
10- Identificação de possíveis outliers.
11- Agrupamentos para identificação de padrões nos dados.
12- Geração do relatório final.
13- Exportação da base tratada para df_limpo.csv.


Base de Dados

O projeto utiliza a base Base Varejo.csv

A base original possui informações relacionadas a:

- Data da compra;
- Identificador da compra;
- Identificador do cliente;
- Gênero do cliente;
- Estado civil;
- Número de filhos;
- Segmento do cliente;
- Identificador do produto;
- Categoria do produto;
- Nome do produto.

Durante a análise inicial também foram encontradas colunas completamente vazias, além de registros duplicados que precisaram ser tratados.

Processo de ETL

ETL significa Extract, Transform e Load (Extração, Transformação e Carregar)

Esse processo é utilizado para extrair dados de uma fonte, realizar os tratamentos necessários e disponibilizar os dados de uma forma mais adequada para análise.

Extração

A etapa de extração consiste em obter os dados da fonte original.

Neste projeto, os dados foram extraídos do arquivo Base Varejo.csv utilizando o módulo csv do Python, por meio do csv.DictReader.

Foi utilizado o caractere `;` como delimitador, pois a base utiliza ponto e vírgula para separar as colunas.

Após a leitura, os dados foram transformados em um DataFrame do Pandas para facilitar as etapas seguintes de tratamento e análise.

Transformação:

A etapa de transformação é responsável por limpar, padronizar e preparar os dados.

Neste projeto foram realizadas as seguintes etapas:

- Padronização de valores do tipo texto;
- Remoção de espaços desnecessários;
- Conversão de colunas numéricas;
- Conversão da coluna de data para o tipo datetime;
- Identificação de valores nulos;
- Tratamento de categorias vazias;
- Remoção de colunas completamente vazias;
- Identificação e remoção de registros duplicados;
- Conversão da coluna de número de filhos para formato numérico;
- Verificação de possíveis valores atípicos (outliers).

Esses tratamentos foram necessários para tornar os dados mais consistentes antes da realização das analises.

Carga

Após as etapas de transformação e limpeza, a base tratada foi exportada para o arquivo:

df_limpo.csv

Esse arquivo representa a versão preparada da base de dados e pode ser utilizado em novas análises com o BI.

Qualidade de Dados

A qualidade dos dados é uma etapa fundamental em um projeto de análise, pois informações incorretas, duplicadas, ausentes ou armazenadas no formato inadequado podem produzir resultados inconsistentes.

Durante este projeto foram analisados alguns aspectos importantes de qualidade dos dados.

Valores Nulos

Foi realizada uma verificação dos valores nulos presentes nas colunas.

As categorias de produtos sem informação foram tratadas utilizando o valor SEM CATEGORIA, evitando a perda desnecessária desses registros.

Também foram identificadas colunas completamente vazias, que foram removidas por não fornecerem informações úteis para a análise.

Registros Duplicados

A base foi analisada para identificar registros completamente duplicados.

Foram encontrados 96.553 registros duplicados, que foram removidos durante o processo de limpeza.

Após esse tratamento, a base ficou sem registros completamente duplicados.

Tipos de Dados

Também foi realizada a conversão dos tipos de dados para formatos adequados.

Os identificadores numéricos foram convertidos para tipos numéricos e a coluna `DATA` foi convertida para `datetime`.

A coluna `CL_FHL`, que representa o número de filhos dos clientes, também foi convertida para formato numérico para permitir o cálculo das estatísticas descritivas.

Datas Inválidas

Durante a conversão da coluna de data foi utilizado um tratamento para identificar valores que não pudessem ser convertidos corretamente.

Na análise realizada não foram identificadas datas inválidas após a conversão.

Resultado do Processo de Limpeza

A base original apresentava:

- 830.000 registros
- 14 colunas

Após o tratamento:

- 733.447 registros
- 10 colunas
- 96.553 registros duplicados removidos
- 0 registros duplicados restantes
- 0 valores nulos restantes
- 0 datas inválidas identificadas

A redução de 14 para 10 colunas ocorreu devido à remoção de quatro colunas completamente vazias.

sobre ETL e Qualidade de Dados

O desenvolvimento deste projeto demonstrou que a análise de dados não começa diretamente com gráficos ou indicadores. Antes de realizar qualquer análise, é necessário compreender a estrutura da base e verificar a qualidade das informações disponíveis.

O processo de ETL foi importante para organizar esse trabalho em etapas. Primeiro, os dados foram extraídos do arquivo CSV. Em seguida, foram transformados por meio da padronização de textos, conversão de tipos, tratamento de valores ausentes e remoção de duplicidades. Por fim, a base tratada foi exportada para um novo arquivo, que representa a etapa de carga.

A qualidade dos dados influencia diretamente a confiabilidade de uma análise. Por exemplo, registros duplicados poderiam aumentar artificialmente a quantidade de compras, enquanto tipos de dados incorretos poderiam impedir cálculos estatísticos ou análises temporais.

Por isso, realizar verificações e tratamentos antes da análise ajuda a reduzir erros e torna os resultados mais confiáveis para apoiar análises e tomadas de decisão.

O miniprojeto permitiu aplicar conceitos importantes de preparação e análise de dados utilizando Python.

A partir de uma base bruta de varejo, foram realizadas etapas de extração, transformação, limpeza, validação e análise exploratória. Como resultado, foi obtida uma base tratada e mais adequada para análises futuras.

O projeto também demonstrou na prática, a importância do processo de ETL e da qualidade dos dados para a construção de análises confiáveis.