# Análise de Dados da Mortalidade por Suicídio no Brasil
### Descrição:

Pesquisas revelam que o Brasil está entre os 10 países onde o suicídio mais acontece. Além dos tratamentos adequados, desmistificar e aprofundar informações e conhecimentos acerca do tema é uma importante estratégia de prevenção. O objetivo deste projeto é extrair informações sobre os registros óbtios por suicídio do sistema de Mortalidade do sistema Datasus, do Ministério da Saúde do Brasil, com dados entre os anos de 2011 a 2021.

Dentre os dados coletados do DATASUS, entre 2011 e 2021 houve um crescimento muito significativo de 62.6% de vidas interrompidas pelo suicídio, considerando que o Brasil apresentou um crescimento populacional aproximado de apenas 11%, segundo dados do IBGE.

Os dados estavam disponíveis no formato CSV para cada ano e utilizei a linguagem Python (3.9.13) para todo o processo de análise de dados. Destaco alguns passos do processo de Análise de Dados:

1. Instalação e importação dos pacotes necessários à análise pretendida (pandas, numpy, so, datetime, timedetla, matplotlib e seaborn);

2. Carregamento dos dados, onde os arquivos CSV estavam disponibilizados por ano de referência. Assim, foi feita uma comparação dentre as colunas dos 10 diferentes DataFrame, com o total de colunas entre 63 e 88, de modo a identificar a equivalência entre as colunas e a importância dentre elas com base das informações disponibilizadas no dicionário de dados e o processo de identificação das variáveis, especialmente, de modo a garantir a anonimização dos dados sensíveis. Concatenação dos DataFrames.

3. Limpeza dos dados: 
3.1. Iniciando pela filtragem, a fim de selecionar os dados que dizem respeito ao projeto, que são os registros com mortalidade pela causa suicídio.

3.2. Verificação do percentual de valores ausentes por coluna.

3.3. Remoção de algumas colunas, seja em razão da fraca interpretabilidade pelo percentual dos valores ausentes, seja aquelas colunas não inerentes à análise ou colunas com valores constantes.

3.4. Remoção de linhas duplicadas.

3.5. Identificação de variáveis com ausência de informação, a exemplo de variáveis constando o símbolo asterisco.

3.6. Formatação de nomes de colunas de modo a compreender melhor os dados.

3.7. Agrupamento por faixa etária das idades de óbito (labels = ['5-14', '15-19', '20-39', '40-59', '60+']), de modo a facilitar o processo de análise.

3.8. Ajuste dos tipos de dados conforme necessário.

3.9. Carregamento do arquivo CSV com os dados dos municípios do sistema DATASUS. Foi identificado que uma coluna tinha mais de uma informação (código e cidade), assim foi utilizado a engenharia de atributos de modo a particionar a coluna. E então, o cruzamento dos dados com o DataFrame principal de modo a constar a descrição do município, utilizando a função "MAP".

4. Análise descritiva de modo a resumir os dados e compreender como os dados estavam organizados e busca de eventuais anomalias. Verificando a Distribuição das Variáveis, verifica-se que o dataset não apresenta variáveis reais numéricas, mas sim variáveis categóricas representadas por números.

4.1. Utilização de estrátegias de imputação de acordo com a especificidade de cada variável, considerando a sensibilidade dos dados em razão de seus aspectos sociais, culturais e demográficos. Além de considerar o percentual de valores nulos e cuidadosamente de modo a não influenciar a distribuição dos dados.

5. Pré-processamento dos dados, respeitando o objetivo do projeto que é a criação de visualizações, criando alguns novos atributos a exemplo do mês do óbito que é um dado revelante à analise (split da "data do óbito"). Além de substitutir as várivaies que apresentam códigos pela abreviação ou descrição respectiva (raça, gênero, estado civil) a fim de facilitar as visualizações. 
6. Comunicação e apresentação dos resultados através de gráficos e story telling através de relatório. No entanto, também foi gerado um CSV resultante para novas visualizações utilizando o Power BI.

### Status do Projeto
Versão 1.0

### Tecnologias utilizadas
Python 3.9.13, Seaborn, Numpy, Pandas, Matplotlib.

### Desenvolvedora do Projeto
Ana Paula Barros Ramos

### Licença
GPL

### Conclusão

Dentre as conclusões, foi observado que o mês de Outubro(10) apresenta um aumento crescente no número de óbitos que se destaca. Constatando-se que o número maior de registros no mês de outubro ocorre em todos os anos da análise, o que sugere uma análise de causa.

Devo salientar que os dados coletados e analisados do sistema DATASUS ainda possibilita diferentes observações, tendo em vista a grande quantidade de variáveis, embora ainda se faz necessário uma melhor coleta e notificação dos dados, considerando que muitas características presentes nos formulários ainda estão ausentes.

O suicídio é um problema de saúde pública, com impactos em toda a sociedade... "Se precisar, peça ajuda!" O telefone 188 do Centro de Valorização da Vida está disponível 24 horas por dia. 

E que para além dos dados e informações, possamos oferecer uma escuta sem pressa, sem banalizar o sofrimento de ninguém.

As informações aqui expostas visam contribuir como parte de estratégias para prevenção do suicídio.

![Alguns Insights](https://media.licdn.com/dms/image/D4D22AQERYWdr3h5dhQ/feedshare-shrink_2048_1536/0/1696468889350?e=1714608000&v=beta&t=HnRPr1mJ4jF5QPbj4tMhzK7qCA7VO0kKcxWDu5X4zrA)

### Contato
LinkedIn: ana-paula-barros-ramos-22a80a198
