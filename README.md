# TRABALHO 01:  SmartSales
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Júlia Suzano Fraga: juliasufraga18@gmail.com<br>

### 2.INTRODUÇÃO E MOTIVAÇAO<br>

> A empresa SmartSales visa auxiliar a gestão de compra e venda de produtos, desde miniempresas a grandes negócios. Com o avanço da tecnologia e a dinamização do mercado, nós como empresa viemos acelerar processos delongados e as vezes falho, resultando, muitas das vezes, em prejuízos a o lojista. Sendo assim, a SmartSales tem como objetivo servir de apoio para o empresário, a fim de agilizar certos processos e contribuir no aumento da lucratividade. Após o cadastro de informações o sistema gerará relatórios que atenderão aos interesses do proprietário.
 

### 3.MINI-MUNDO Novo<br>

> O sistema proposto pela SmartSales conterá as informações aqui detalhadas. Inicialmente serão cadastradas todas as informações referentes aos fornecedores, englobadas nas tabelas Fornecedo, contendo código e nome dos fornecedores, Ramo, com código e o ramo do fornecedor e por fim o conjunto contato, caracterizado pelas tabelas Contato, incluindo o contato e o código do mesmo, e por fim a tabela Tipo, caracterizando o contato com  o nome e o código do tipo do contato. Em seguida serão inseridas os dados na tabela Cliente, que agrupa informações de cada cliente, como por exemplo código, nome, sexo, data de nascimento e as cordenadas geograficas dos clientes.  Com o cadastro de código, data e preço de aquisição preenchemos a tabela Aquisição, afim de controlar a entrada dos produtos, e logo após a tabela Produto poderá ser preenchida com código, nome e preço de venda dos produtos. Por fim será completada a tabela Compra com código e data das compras efutuadas, marcando assim a saída dos produtos. Ao decorrer dos relacionamentos entre estas tabelas, três destes formam outras novas tabelas, sendo estas tabelas de relacionamento. São essas as tabelas Itens, contendo as chaves estrangeiras das tabelas produto e compra, mais código  itens, servindo como uma espécie de lista dos produtos comprados, e quantidade de venda, a tabela Produro_Aqusicao armazenando as chaves estrangeiras das tabelas produro e aquisição, mais a quantidade de aquisição e um código identificador, e por último temos a tabela Pertence, que contém unicamente as chaves de da tabela fornecedor e ramo.  A partir dessas entidades, o sistema já está pronto para computar sua função principal, a saída e entrada de produtos. 


### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto consta o pdf com o rascunho da interface do nosso programa.  <br>

![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/menu%20incial%20SS.jpg?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para SmartSales](https://github.com/SS-SmartSales/trabalho01/blob/master/novo%20Mini%20Mundo.pdf?raw=true "Empresa Devcom")


#### 4.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
 
*Qual o fornecedor com os produtos com o melhor preço?

*Quantos produtos tem em estoque?

*Qual o produto menos e mais vendidos?

*Quanto foi a despesa e lucro sobre os produtos?

*Qual o público-alvo dos produtos?
 

#### 4.2 TABELA DE DADOS DO SISTEMA:

>A tabela aqui anexada contém os atributos do sistema SmartSales. Ela simula um relatório com todos os dados que serão armazenados.

    CLIENTE: Contém as informações dos clientes da empresa.
    COMPRA: Identifica e data uma a compra.
    ITENS: Lista e quantifica os itens vendidos.
    PRODUTO: Codifica, nomeia e estabelece o preço de venda.
    CATEGORIA: Categoriza os produtos.
    PRODUTO_AQUSICAO: Quantifica os produtos comprados.
    AQUISICAO: Controla a entrada dos produtos e caracteriza preço de aquisição.
    FORNECEDO: Identifica o fornecedor com nome e código.
    RAMO: Determina o ramo do fornecedor.
    CONTATO: Armazena e codifica o contato do fornecedor.
    TIPO: Categoriza o tipo de contato do fornecedor.
    
    
![Exemplo de Tabela de dados da SmartSales](https://github.com/SS-SmartSales/trabalho01/blob/master/nova%20PlanilhaSmartsSales%20%20em%20ods.ods?raw=true "Tabela - SmartSales")

### 5.MODELO CONCEITUAL<br>

> O modelo conceitual apresenta as entidades existentes no programa e os relacionamentos que elas possuem entre si.
    
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/MODELOCONCEITUAL.jpeg)
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Lucas Tejada Fabres e Caio Simão Lessa]
    [Grupo02]: [Rodolfo Luiz de Oliveira e Gustavo Olmo Santana]

#### 5.2 DESCRIÇÃO DOS DADOS 
   
	Tabela Cliente
NOME: nome do cliente.
SEXO: sexo do cliente.
DATA_NASCIMENTO: data de nascimento do cliente.
LATITUDE: latitude da residência.
LONGITUDE: longitude da residência. 
CODIGO: código identificador do cliente.

	Tabela Compra
CODIGO_COMPRA: código identificador da compra.
DATA: data que a compra foi efetuada.

	Tabela Itens
QTD_VENDA: quantidade do produro que vai ser comprado.
COD_ITENS: código identificador do cliente.

	Tabela Produto
CODIGO_PRODUTO: código identificador do produto.
NOME: nome do produto.
PRECO_VENDA: preço de venda do produto.

	Tabela Categoria
COD_CATEGORIA: código identificador da categoria.
TIPO: nome do tipo de categoria.

	Tabela Produto_Aqusicao
COD: código identificador de produto_aquisição.
QTD_AQUISICAO:quantidade do produto adquirido.

	Tabela Aquisicao
CODIGO: código identificador da aquisição.
DATA: data da aquisição do produto.
PRECO_AQUISICAO: preço da aquisição do produto.

	Tabela Fornecedo
CODIGO: código identificador do fornecedor.
NOME: nome do fornecedor.

	Tabela Ramo
COD_RAMO: código identificador do ramo.
RAMO: nome do ramo.

	Tabela Contato
CODIGO_CONTATO: código identificador do contato.
CONTATO: contato do fornecedor.

	Tabela Tipo
TIPO: nome do tipo do contato.
COD_TIPO: código identificador do tipo de contato.

    
    
### 6	MODELO LÓGICO<br>

> Aqui consta o modelo lógico do trabalho realizado pelo grupo.

![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/MODELOLOGICO.jpeg)

### 7	MODELO FÍSICO<br>

    /* Lógico_1: */

    CREATE TABLE PRODUTO (
    	codigo integer PRIMARY KEY,
   	nome varchar(30),
  	preco_aquisicao float,
  	tipo varchar(30),
  	data_aquisicao date,
 	qtd_adquirirda integer,
  	preco_venda floa
    );

    CREATE TABLE CLIENTE (
   	 codigo integer PRIMARY KEY,
  	 nome varchar(100),
  	 sexo char,
         idade integer
    );

    CREATE TABLE COMPRA (
    	numero_nota integer PRIMARY KEY,
    	data_compra date,
    	qtd_venda integer,
    	desconto float
    );

    CREATE TABLE Fornecedor (
    	codigo integer PRIMARY KEY,
    	nome varchar(30),
    	ramo varchar(30),
    	contato varchar(15)
    );

    CREATE TABLE realiza (
    	fk_CLIENTE_codigo integer,
    	fk_COMPRA_numero_nota integer
    );

    CREATE TABLE Possui (
    	fk_COMPRA_numero_nota integer,
    	fk_PRODUTO_codigo integer
    );

    CREATE TABLE Fornece (
    	fk_Fornecedor_codigo integer,
    	fk_PRODUTO_codigo integer
    );
 
    ALTER TABLE realiza ADD CONSTRAINT FK_realiza_1
    	FOREIGN KEY (fk_CLIENTE_codigo)
    	REFERENCES CLIENTE (codigo)
    	ON DELETE RESTRICT;
 
    ALTER TABLE realiza ADD CONSTRAINT FK_realiza_2
    	FOREIGN KEY (fk_COMPRA_numero_nota)
    	REFERENCES COMPRA (numero_nota)
    	ON DELETE RESTRICT;
 
    ALTER TABLE Possui ADD CONSTRAINT FK_Possui_1
    	FOREIGN KEY (fk_COMPRA_numero_nota)
    	REFERENCES COMPRA (numero_nota)
    	ON DELETE RESTRICT;
 
    ALTER TABLE Possui ADD CONSTRAINT FK_Possui_2
    	FOREIGN KEY (fk_PRODUTO_codigo)
    	REFERENCES PRODUTO (codigo)
    	ON DELETE RESTRICT;
 
    ALTER TABLE Fornece ADD CONSTRAINT FK_Fornece_1
    	FOREIGN KEY (fk_Fornecedor_codigo)
    	REFERENCES Fornecedor (codigo)
    	ON DELETE RESTRICT;
 
    ALTER TABLE Fornece ADD CONSTRAINT FK_Fornece_2
    	FOREIGN KEY (fk_PRODUTO_codigo)
    	REFERENCES PRODUTO (codigo)
    	ON DELETE RESTRICT;
    
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        
    INSERT INTO
	       COMPRA
    VALUES  (12, '2019-04-07', 001, 1, 0.0, 1111),
	           (12, '2019-04-07', 002, 1, 0.0, 1111),
	           (12, '2019-04-07', 003, 2, 0.2, 1111),
	           (12, '2019-04-07', 005, 10, 0.0, 1111),
	           (16, '2019-04-08', 006, 2, 0.0, 3333),
	           (17, '2019-04-08', 008, 1, 0.0, 2222),
	           (18, '2019-04-10', 003, 1, 0.0, 6666),
	           (19, '2019-04-11', 007, 1, 0.0, 4444),
	           (20, '2019-04-11', 004, 1, 0.0, 5555),
	           (20, '2019-04-11', 009, 1, 0.0, 5555);

    INSERT INTO
        PRODUTO
    VALUES  (001, 'Tênis rosa', 44444444, 'tênis', 30, 50, '2019-03-11', 130),
	           (002, 'Tênis branco', 44444444, 'tênis', 30, 50, '2019-03-11', 130),
	           (003, 'Tênis preto', 44444444, 'tênis', 50, 50, '2019-03-11', 130),
	           (004, 'Meia Puma', 22222222, 'meia', 40, 17.60, '2019-03-12', 47.90),
	           (005, 'Sapatilha Preta', 55555555, 'sapatilha', 35, 48, '2019-03-15', 120),
	           (006, 'Bota feminina',33333333, 'bota', 20, 89.90, '2019-03-22', 240),
	           (007, 'Sapato masculino', 77777777, 'sapato social', 50, 78.75, '2019-04-07', 160),
	           (008, 'Sapatilha vermelha', 66666666, 'sapatilha', 60, 53.55, '2019-03-15', 180),
           	(009, 'Meia Adidas', 11111111, 'meia', 50, 18.30, '2019-03-12', 47.90),
	           (010, 'Alpargata', 88888888, 'alpargata', 40, 14, '2019-04-04', 130);

    INSERT INTO
	       FORNECEDOR
    VALUES  (44444444, 'Converse', 'Tênis', '(44)4444-4444'),
	           (22222222, 'Puma', 'Esportes', '(22)2222-2222'),
	           (55555555, 'Moleca', 'Calçados Femininos', '(55)5555-5555'),	
	           (33333333, 'Vizzano', 'Calçados Femininos', '(33)3333-3333'),
	           (77777777, 'Luis Vuitton', 'Vestuário', '(77)7777-7777'),
	           (66666666, 'Arezzo', 'Calçados Femininos', '(66)6666-6666'),
	           (11111111, 'Adidas', 'Esportes', '(11)1111-1111'),
	           (88888888, 'Marriano', 'Sapatos', '(88)8888-8888');

    INSERT INTO
	        CLIENTE
    VALUES  (1111, 'Joana', 40, 'F'),
           	(3333, 'Maria', 41, 'F'),
	           (2222, 'Marcos', 38, 'M'),
	           (6666, 'Amanda', 28, 'F'),
	           (4444, 'Valéria', 35, 'F'),
	           (5555, 'Jonas', 43, 'M');

##Junção

    /* Lógico_1: */

    CREATE TABLE PRODUTO (
     codigo integer PRIMARY KEY,
     nome varchar(30),
     fornecedor integer,
     tipo varchar(30),
     quantidade_adquirida integer,
     preco_aquisicao float,
     data_aquisicao date,
     preco_venda float
    );

    CREATE TABLE CLIENTE (
     codigo integer,
     nome varchar(100),
     idade integer,
     sexo char
    );
    
    CREATE TABLE COMPRA (
     numero_nota integer,
     data_compra date,
     produto integer,
     qtd_venda integer,
     desconto float,
     cliente integer
    );

    CREATE TABLE Fornecedor (
     codigo integer PRIMARY KEY,
     nome varchar(30),
     ramo varchar(30),
     contato varchar(15)
    );
     
     INSERT INTO
	       COMPRA
    VALUES  (12, '2019-04-07', 001, 1, 0, 1111),
	           (12, '2019-04-07', 002, 1, 0, 1111),
	           (12, '2019-04-07', 003, 2, 0.2, 1111),
	           (12, '2019-04-07', 005, 10, 0, 1111),
	           (16, '2019-04-08', 006, 2, 0, 3333),
	           (17, '2019-04-08', 008, 1, 0, 2222),
	           (18, '2019-04-10', 003, 1, 0, 6666),
	           (19, '2019-04-11', 007, 1, 0, 4444),
	           (20, '2019-04-11', 004, 1, 0, 5555),
	           (20, '2019-04-11', 009, 1, 0, 5555);

    INSERT INTO
        PRODUTO
    VALUES  (001, 'Tênis rosa', 44444444, 'tênis', 30, 50, '2019-03-11', 130),
	           (002, 'Tênis branco', 44444444, 'tênis', 30, 50, '2019-03-11', 130),
	           (003, 'Tênis preto', 44444444, 'tênis', 50, 50, '2019-03-11', 130),
	           (004, 'Meia Puma', 22222222, 'meia', 40, 17.60, '2019-03-12', 47.90),
	           (005, 'Sapatilha Preta', 55555555, 'sapatilha', 35, 48, '2019-03-15', 120),
	           (006, 'Bota feminina',33333333, 'bota', 20, 89.90, '2019-03-22', 240),
	           (007, 'Sapato masculino', 77777777, 'sapato social', 50, 78.75, '2019-04-07', 160),
	           (008, 'Sapatilha vermelha', 66666666, 'sapatilha', 60, 53.55, '2019-03-15', 180),
           	(009, 'Meia Adidas', 11111111, 'meia', 50, 18.30, '2019-03-12', 47.90),
	           (010, 'Alpargata', 88888888, 'alpargata', 40, 14, '2019-04-04', 130);

    INSERT INTO
	       FORNECEDOR
    VALUES  (44444444, 'Converse', 'Tênis', '(44)4444-4444'),
	           (22222222, 'Puma', 'Esportes', '(22)2222-2222'),
	           (55555555, 'Moleca', 'Calçados Femininos', '(55)5555-5555'),	
	           (33333333, 'Vizzano', 'Calçados Femininos', '(33)3333-3333'),
	           (77777777, 'Luis Vuitton', 'Vestuário', '(77)7777-7777'),
	           (66666666, 'Arezzo', 'Calçados Femininos', '(66)6666-6666'),
	           (11111111, 'Adidas', 'Esportes', '(11)1111-1111'),
	           (88888888, 'Marriano', 'Sapatos', '(88)8888-8888');

    INSERT INTO
	        CLIENTE
    VALUES  (1111, 'Joana', 40, 'F'),
           	(3333, 'Maria', 41, 'F'),
	           (2222, 'Marcos', 38, 'M'),
	           (6666, 'Amanda', 28, 'F'),
	           (4444, 'Valéria', 35, 'F'),
	           (5555, 'Jonas', 43, 'M');
        
        

## Marco de Entrega 08 em: (29/05/2019)<br>

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/Produto.png)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/Fornecedor.png)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/Compra.png)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/Cliente.png)

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas
#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.


    
#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>


#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>
        a) Uma junção que envolva todas as tabelas possuindo no mínimo 3 registros no resultado
        b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho
        

### ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO SEMESTRAL (Mínimo 6 e Máximo 10)<br>


#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4)<br>
#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho
#### 9.10	SUBCONSULTAS (Mínimo 3)<br>

#### 9.11	LISTA DE CODIGOS DAS FUNÇÕES E TRIGGERS<br>
        Detalhamento sobre funcionalidade de cada código.
        a) Objetivo
        b) Código do objeto (função/trigger)
        c) exemplo de dados para aplicação
        d) resultados em forma de tabela/imagem
<br>


#### 9.12	GERACAO DE DADOS (MÍNIMO DE 100 MIL REGISTROS PARA PRINCIPAL RELAÇAO)<br>
        a) principal tabela do sistema deve ter no mínimo 100 mil registros
        b) tabelas diretamente relacionadas a tabela principal 10 mil registros
        c) tabelas auxiliares de relacao multivalorada mínimo de 10 registros
        d) registrar o tempo de inserção em cada uma das tabelas do banco de dados
        e) especificar a quantidade de registros inseridos em cada tabela
        Para melhor compreensão verifiquem o exemplo na base de testes:<br>
        https://github.com/discipbd2/base-de-testes-locadora
        

#### 9.13	Backup do Banco de Dados<br>
        Detalhamento do backup.
        a) Tempo
        b) Tamanho
        c) Teste de restauração (backup)
        d) Tempo para restauração
        e) Teste de restauração (script sql)
        f) Tempo para restauração (script sql)
<br>

Data de Entrega: (Data a ser definida)
<br>

#### 9.14	APLICAÇAO DE ÍNDICES E TESTES DE PERFORMANCE<br>
    a) Lista de índices, tipos de índices com explicação de porque foram implementados nas consultas 
    b) Performance esperada VS Resultados obtidos
    c) Tabela de resultados comparando velocidades antes e depois da aplicação dos índices (constando velocidade esperada com planejamento, sem indice e com índice Vs velocidade de execucao real com índice e sem índice).
    d) Escolher as consultas mais complexas para serem analisadas (consultas com menos de 2 joins não serão aceitas)
    e) As imagens do Explain devem ser inclusas no trabalho, bem como explicações sobre os resultados obtidos.
    f) Inclusão de tabela mostrando as 10 execuções, excluindo-se o maior e menor tempos para cada consulta e 
    obtendo-se a media dos outros valores como resultado médio final.
<br>
    Data de Entrega: (Data a ser definida)
<br>   

### 10	ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO FINAL (Mínimo 6 e Máximo 10)<br>
<br>
    Data de Entrega: (Data a ser definida)
<br>

### 11 Backup completo do banco de dados postgres 
    a) deve ser realizado no formato "backup" 
        (Em Dump Options #1 Habilitar opções Don't Save Owner e Privilege)
    b) antes de postar o arquivo no git o mesmo deve ser testado/restaurado por outro grupo de alunos/dupla
    c) informar aqui o grupo de alunos/dupla que realizou o teste.

    
### 12	TUTORIAL COMPLETO DE PASSOS PARA RESTAURACAO DO BANCO E EXECUCAO DE PROCEDIMENTOS ENVOLVIDOS NO TRABALHO PARA OBTENÇÃO DOS RESULTADOS<br>
        a) Outros grupos deverão ser capazes de restaurar o banco 
        b) executar todas as consultas presentes no trabalho
        c) executar códigos que tenham sido construídos para o trabalho 
        d) realizar qualquer procedimento executado pelo grupo que desenvolveu o trabalho

### 13	DIFICULDADES ENCONTRADAS PELO GRUPO<br>  

    
Data de Entrega final: (Data a ser definida)
<br>

       
### 14  FORMATACAO NO GIT: https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
   
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/

#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. Caso existam arquivos com conteúdos sigilosos, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário deste GIT, para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://sis4.com/brModelo/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


        
        


    





