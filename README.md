# simulator_Telos_nivel0
Este repositório contém os arquivos necessários para o Projeto Simulator Nível 0 da Seleção AfroDigital Télos Tech


## Análise de Dados da Empresa ABC

### Descrição do Projeto

Este projeto tem como objetivo analisar os dados de vendas da Empresa ABC, uma varejista online que opera em diversos países. O foco é entender o comportamento do cliente, identificar produtos de alta demanda e otimizar as operações de vendas. Para isso, o projeto utiliza um banco de dados SQLite, a biblioteca Pandas do Python para manipular e analisar os dados e o DB Browser for SQLite para visualizar os dados no banco de dados.

## Contextualização

Neste exercício, você vai mergulhar no mundo da manipulação de dados usando uma combinação de Python, SQL, e técnicas de análise de dados. Você vai criar uma tabela de dados, usar o GPT para gerar um conjunto de dados ﬁctício, inserir esses dados em um banco de dados SQLite, e os manipular utilizando a biblioteca pandas para responder a várias perguntas de negócio. Este exercício irá equipá-lo com habilidades práticas em ciência de dados, manipulação e análise de dados que são cruciais em muitas áreas da tecnologia e negócios hoje..

## Descrição

A Empresa ABC é uma varejista online que vende uma variedade de produtos, desde eletrônicos até vestuário. Eles operam em vários países e têm uma base de clientes diversiﬁcada. Recentemente, a empresa decidiu analisar seu banco de dados de vendas para melhor entender o comportamento do cliente, identiﬁcar produtos de alta demanda e otimizar suas operações de vendas. Para isso, eles precisam analisar seus dados de vendas, que incluem informações sobre clientes, pedidos, produtos e transações.

## Dados Necessários

CLIENTES: ID do Cliente, Nome, País

PRODUTOS: ID do Produto, Nome do Produto, Categoria, Preço  

PEDIDOS: ID do Pedido, ID do Cliente, Data do Pedido 

DETALHES DO PEDIDO: ID do Pedido, ID do Produto, Quantidade

## Seções de Perguntas de Negócio

Análise de Clientes
1.	Quais são os top 5 países em número de clientes?
2.	Quantos clientes únicos realizaram mais de um pedido?
3.	Qual é o valor médio de pedidos por cliente em cada país?
4.	Quais são os 3 principais clientes em termos de valor total de pedidos?

Análise de Produtos
1.	Quais são as top 5 categorias de produtos mais vendidas?
2.	Qual é o produto mais caro que foi vendido?
3.	Qual categoria de produto gera a maior receita?
4.	Quais são os top 3 produtos mais vendidos?

Análise de Pedidos
1.	Qual é o número total de pedidos realizados por mês?
2.	Qual é o valor médio de um pedido?
3.	Quais são os dias da semana com mais pedidos?
4.	Qual é o país com o maior número de pedidos?

Análise de Tendências de Vendas
1.	Como as vendas de cada categoria de produto mudaram ao longo do ano?
2.	Existe alguma correlação entre o país do cliente e a categoria de produto comprada?
3.	Como o valor médio do pedido varia por mês?
4.	Qual categoria de produto mostra a maior variação de vendas entre os meses?



### Funcionalidades do Programa em Python

O script Python realiza as seguintes tarefas:

* **Cria as tabelas do banco de dados:** Cria as tabelas `Clientes`, `Produtos`, `Pedidos` e `Detalhes_Pedidos` no banco de dados SQLite.
* **Lê dados de arquivos CSV:**  Carrega dados dos arquivos CSV `clientes.csv`, `Produtos.csv`, `Pedidos.csv` e `detalhesPedido.csv` para DataFrames do Pandas.
* **Converte tipos de dados:** Converte a coluna `Data_Pedido` para o formato de data e as colunas numéricas para o tipo inteiro.
* **Insere dados nas tabelas:** Insere os dados dos DataFrames nas tabelas correspondentes no banco de dados SQLite.

### Como executar o projeto

Para executar o projeto, siga estes passos:

1. **Criar um banco de dados SQLite:**
   * Crie um arquivo chamado `empresa_abc.db` na mesma pasta do script Python.
2. **Criar os arquivos CSV:**
   * Crie os arquivos `clientes.csv`, `Produtos.csv`, `Pedidos.csv` e `detalhesPedido.csv` com os dados da Empresa ABC.
3. **Executar o script Python:**
   * Execute o script Python que contém o código fornecido.

### Desafios encontrados

Foi preciso ver alguns tutoriais em vídeos no Youtube para entender bem a sistemática da conexão com o SQLite dentro do Python.
O maior desafio foi inserir os dados na tabela `Detalhes_Pedidos`.  Apesar de ter definido o tipo de dados da coluna `Quantidade` como `INTEGER` no banco de dados, os dados estavam sendo armazenados como BLOB. Tive que investigar vários erros e soluções antes de descobrir que o problema estava na forma como a conexão com o banco de dados estava sendo gerenciada no código.  

### Resultados e lições Aprendidas

O código final conseguiu inserir os dados corretamente em todas as tabelas do banco de dados. Aprendi a importância de:

* **Gerenciar a conexão com o banco de dados:**  Manter a mesma conexão e o mesmo cursor durante todo o script para evitar problemas.
* **Verificar os tipos de dados:**  Garantir que os tipos de dados das colunas no banco de dados sejam consistentes com os dados que você está inserindo.
* **Utilizar a ferramenta de depuração do Python:**  Usar a função `print` para verificar os valores das variáveis e a execução do código.

### Próximos passos

* **Realizar análises mais complexas:**  Explorar outras técnicas de análise de dados para extrair insights mais profundos, como análise de regressão, análise de cluster e análise de séries temporais.
* **Criar dashboards:**  Visualizar os resultados das análises usando dashboards interativos para apresentar as informações de forma clara e concisa.
* **Automatizar o processo de análise:**  Criar scripts para automatizar a coleta de dados, o processamento, a análise e a geração de relatórios.

### Captura de telas


PROMPTs de comando usados para criar as bases de dados necessárias para o projeto. As bases de daos foram criadas usando a Gemini do Google:

![promtp01](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/77eacacc-ef17-4ee1-90e5-8b2e906802e9)

![promtp02](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/2b18151d-decc-4469-b06b-56cfde85442e)

![promtp03](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/65201568-68a1-4359-824f-7097ecef88ca)

![promtp04](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/31ae0d75-6095-47b8-bde1-0a252ac8fedc)


Imagens dos conteúdos dos arquivos em CSV :

Clientes.csv

![csv001](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/883556fd-67c3-4a32-b887-ec87b84b3a64)

Produtos.csv

![csv002](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/2d7e55e9-df9e-450e-8183-4bdbb968e989)

Pedidos.csv

![csv003](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/a889e09a-59bb-4a3a-946b-cdfdec965895)

detalhesPedido.csv

![csv004](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/08be8c8d-4239-42bd-948f-a1397889c983)

Respostas para as Perguntas de Negócio:

![colab001](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/af8d6f98-4afa-471e-84c7-1d91dd6e71cb)

![colab002](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/93182980-afd7-46af-9192-6b538b75c75b)

![colab003](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/cb1f0d1b-8d34-4a6d-91f7-ab2d7921073a)

![colab004](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/44cdbbdf-7528-4484-a2f2-8d9287e55267)

![colab005](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/88e8c7c0-32a6-4ac6-a201-307161d9e23d)

![colab006](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/cb08e8af-87ad-4f1c-a784-d399db23f437)

![colab007](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/06b7f075-0fe6-4fb2-ab80-0c83e79ef368)

![colab008](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/3e6aa0b5-b1ec-4e6b-a553-d13f09276b95)

![colab009](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/ac86ff77-ccd8-4b21-bc2d-e1690878671f)

![colab010](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/46f1f7d0-799a-46f4-9b62-3349572990c9)

![colab011](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/4197b0f9-107c-41d7-b310-ac99a305ee83)

![colab012](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/1dfbcd22-52a8-4621-a8ac-c9be7d37bf73)

![colab013](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/35b20902-688e-4d36-8c49-90c5616815b7)

![colab014](https://github.com/enps2015/simulator_Telos_nivel0/assets/84017071/afd0e586-5dd1-42f6-8aed-cd464d6d8aec)






















