### Introdução

Bem-vindo ao Desafio de Código da Framework!

Essa é uma oportunidade para você mostrar sua pegada 

Esta é uma oportunidade para você nos mostrar sua compreensão do SQL, que desempenha um papel fundamental no trabalho do dia-a-dia para o qual você está se candidatando. Todos os membros da equipe do Framework Data aceitaram esse desafio e participaram de sua criação. Se você achar que há perguntas que não são justas ou não são claras, por favor nos avise; Isso é muito importante para nós!

Algumas coisas importantes a serem observadas antes de começar:

- Se você não puder responder a uma pergunta, faça o seu melhor, mostre seu trabalho, deixe comentários e deixe-nos saber seus pensamentos gerais.
- Estamos interessados em suas respostas e no trabalho/código que você escreve para obtê-las. Por favor, deixe muitos comentários para nós lermos quando revisarmos seu trabalho.
- Existem alguns valores em branco/nulos neste conjunto. Foi assim que o encontramos e reflete a natureza dos dados imperfeitos. Trabalhe com isso e forneça explicações sobre quaisquer problemas ou soluções alternativas necessárias para chegar às suas respostas.
- Não há pegadinhas intencionais, perguntas capciosas ou armadilhas; o desafio visa demonstrar algumas das habilidades típicas de SQL do dia-a-dia que o trabalho exige.
- Algumas dessas perguntas podem parecer sem sentido e você pode se perguntar: "por que alguém iria querer saber isso?!" Eles são destinados puramente como uma medida da suas habilidades de SQL e não como perguntas reais que esperaríamos fazer a esse tipo de conjunto de dados.

### Instruções

- Crie um banco de dados SQL usando os arquivos CSV em anexo.
- Use o banco de dados para responder às seguintes perguntas.
- Todas as respostas que retornam valores monetários devem ser arredondadas para 2 casas decimais e precedidas do símbolo "$" (por exemplo, "$1432,10").
- Todas as respostas que retornam valores percentuais devem estar entre -100,00 e 100,00, arredondadas para 2 casas decimais e seguidas do símbolo "%" (por exemplo, "58,30%").
- Copie e cole as perguntas da seção abaixo em um novo arquivo .txt simples chamado: {firstname}_{lastname}_code_challenge.txt (por exemplo, "john_smith_code_challenge.txt").
- Fornecer todos os resultados do seu trabalho como respostas; não podemos avaliar seu trabalho sem os resultados da sua consulta!
- Forneça todo o código, incluindo o que você usou para criar o banco de dados e importar os dados, e as respostas relacionadas a cada pergunta imediatamente abaixo da pergunta.
- Sinta-se à vontade para deixar muitos comentários para nos ajudar a entender seu trabalho.
- Quando estiver pronto, responda a este e-mail e anexe seus resultados.
- *GDP* == *PIB*

### Code Challenge

1\. Integridade dos dados: Verificação e limpeza

- Liste em ordem alfabética todos os códigos de país na tabela continente_map que aparecem mais de uma vez. Exiba quaisquer valores em que country_code seja nulo como country_code = "FOO" e faça com que essa linha apareça primeiro na lista, mesmo que ela deva ser classificada em ordem alfabética no meio. Forneça os resultados desta consulta como sua resposta.

- Para todos os países que possuem várias linhas na tabela continente_map, exclua todos os vários registros deixando apenas 1 registro por país. O registro que você mantém deve ser o primeiro quando classificado pelo continente_code em ordem alfabética crescente. Forneça as consultas e as explicações das etapas que você seguiu para excluir esses registros.

2\. Liste os países que tiveram crescimento de 10 a 12 por cento entre os anos de 2011 a 2012.

O percentual de crescimento deve ser calculado como: ((PIB de 2012 - PIB de 2011) / PIB de 2011)

A lista deve incluir as colunas:

- rank
- continent_name
- country_code
- country_name
- growth_percent

3\. Para o ano de 2012, crie um relatório de 3 colunas e 1 linha mostrando a porcentagem de participação de gdp_per_capita para as seguintes regiões:

(i) Ásia, (ii) Europa, (iii) o Resto do mundo. Seu resultado deve ser algo como:

 Asia  | Europe | Rest of World 
------ | ------ | -------------
25.0%  | 25.0%  | 50.0%

4a\. Qual é a contagem de países e a soma de seus valores gdp_per_capita relacionados para o ano de 2007 em que a string 'an' (não diferenciar maiúsculas de minúsculas) aparece em qualquer lugar no nome do país?

4b\. Repita a pergunta 4a, mas desta vez torne a consulta sensível a maiúsculas e minúsculas.

5\. Encontre a soma de gdp_per_capita por ano e a contagem de países para cada ano que tem pib per capita (gdp_per_capita) não nulo onde (1) o ano é anterior a 2012 e (2) o país tem o gdp_per_capita nulo em 2012. Seu resultado deve ter as colunas:

- year
- country_count
- sum_gdp_per_capita

6\. Em uma única consulta, execute todas as etapas abaixo e forneça os resultados como sua resposta final:

a. crie lista única de todos os registros per_capita para o ano de 2009 que inclua colunas:

- continent_name
- country_code
- country_name
- gdp_per_capita

b. ordene esta lista por:

- continent_name de forma ascendente
- caracteres de 2 a 4 do country_name de forma descendente

c. crie um total de gdp_per_capita por continente_name

7\. Encontre o país com a maior média de gdp_per_capita para cada continente em todos os anos. Agora compare sua lista com o seguinte conjunto de dados. Descreva todos e quaisquer erros que você possa encontrar com o conjunto de dados abaixo. Inclua qualquer código usado para ajudar a detectar esses erros.

rank | continent_name | country_code | country_name | avg_gdp_per_capita 
---- | -------------- | ------------ | ------------ | -----------------
   1 | Africa         | SYC          | Seychelles   |         $11,348.66
   1 | Asia           | KWT          | Kuwait       |         $43,192.49
   1 | Europe         | MCO          | Monaco       |        $152,936.10
   1 | North America  | BMU          | Bermuda      |         $83,788.48
   1 | Oceania        | AUS          | Australia    |         $47,070.39
   1 | South America  | CHL          | Chile        |         $10,781.71
