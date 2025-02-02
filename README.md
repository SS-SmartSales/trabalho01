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
 
	
		*Dentre os fornecedores, quais possuem o menor preço dentre uma lista de produtos.
		*Quantidade de elementos para cada produto existente no estoque ordenados pelos que possuem menor quantidade.
		*Qual foi os produtos que foi mais vendidos? E os menos vendidos?
		*Quanto foi valor gasto e o valor adquirido referente a um determinado produto?
		*Qual o público-alvo de um produto de acordo com a idade do cliente


#### 4.2 TABELA DE DADOS DO SISTEMA:

>A tabela aqui anexada contém os atributos do sistema SmartSales. Ela simula um relatório com todos os dados que serão armazenados.

    CLIENTE: Contém as informações dos clientes da empresa.
    COMPRA: Identifica e data uma a compra.
    ITENS: Lista e quantifica os itens vendidos.
    PRODUTO: Codifica, nomeia e estabelece o preço de venda.
    CATEGORIA: Categoriza os produtos.
    PRODUTO_AQUSICAO: Quantifica os produtos comprados.
    AQUISICAO: Controla a entrada dos produtos e caracteriza preço de aquisição.
    FORNECEDOR: Identifica o fornecedor com nome e código.
    RAMO: Determina o ramo do fornecedor.
    CONTATO: Armazena e codifica o contato do fornecedor.
    TIPO: Categoriza o tipo de contato do fornecedor.
    
    
![Exemplo de Tabela de dados da SmartSales](https://github.com/SS-SmartSales/trabalho01/blob/master/nova%20PlanilhaSmartsSales%20%20em%20ods.ods?raw=true "Tabela - SmartSales")

### 5.MODELO CONCEITUAL<br>

> O modelo conceitual apresenta as entidades existentes no programa e os relacionamentos que elas possuem entre si.
    
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/111.PNG)
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Lucas Tejada Fabres e Caio Simão Lessa]
    [Grupo02]: [Rodolfo Luiz de Oliveira e Gustavo Olmo Santana]

#### 5.2 DESCRIÇÃO DOS DADOS 
   
	Tabela Cliente

		*NOME: nome do cliente.

		*SEXO: sexo do cliente.

		*DATA_NASCIMENTO: data de nascimento do cliente.

		*LATITUDE: latitude da residência.

		*LONGITUDE: longitude da residência. 

		*CODIGO: código identificador do cliente.

	Tabela Compra

		*CODIGO_COMPRA: código identificador da compra.

		*DATA: data que a compra foi efetuada.

		Tabela Itens

		*QTD_VENDA: quantidade do produro que vai ser comprado.

		*COD_ITENS: código identificador do cliente.

	Tabela Produto

		*CODIGO_PRODUTO: código identificador do produto.

		*NOME: nome do produto.

		*PRECO_VENDA: preço de venda do produto.

	Tabela Categoria

		*COD_CATEGORIA: código identificador da categoria.

		*TIPO: nome do tipo de categoria.

	Tabela Produto_Aqusicao

		*COD: código identificador de produto_aquisição.

		*QTD_AQUISICAO:quantidade do produto adquirido.

	Tabela Aquisicao

		*CODIGO: código identificador da aquisição.

		*DATA: data da aquisição do produto.

		*PRECO_AQUISICAO: preço da aquisição do produto.

	Tabela Fornecedor

		*CODIGO: código identificador do fornecedor.

		*NOME: nome do fornecedor.

		Tabela Ramo

		*COD_RAMO: código identificador do ramo.

		*RAMO: nome do ramo.

	Tabela Contato

		*CODIGO_CONTATO: código identificador do contato.

		*CONTATO: contato do fornecedor.

	Tabela Tipo

		*TIPO: nome do tipo do contato.

		*COD_TIPO: código identificador do tipo de contato.

    
    
### 6	MODELO LÓGICO<br>

> Aqui consta o modelo lógico do trabalho realizado pelo grupo.

![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/222.PNG)

### 7	MODELO FÍSICO<br>

	CREATE TABLE CLIENTE (
	    nome varchar(50),
	    sexo char,
	    data_nascimento Date,
	    latitude float,
	    longitude float,
	    codigo integer PRIMARY KEY
	);

	CREATE TABLE PRODUTO (
	    codigo_produto integer PRIMARY KEY,
	    nome varchar(50),
	    preco_venda float,
	    FK_CATEGORIA_cod_categoria integer
	);

	CREATE TABLE FORNECEDOR (
	    nome varchar(50),
	    codigo integer PRIMARY KEY
	);

	CREATE TABLE CONTATO (
	    codigo_contato integer PRIMARY KEY,
	    contato varchar(30),
	    FK_FORNECEDOR_codigo integer,
	    FK_TIPO_cod_tipo integer
	);

	CREATE TABLE CATEGORIA (
	    cod_categoria integer PRIMARY KEY,
	    tipo varchar(30)
	);

	CREATE TABLE COMPRA (
	    cod_compra integer PRIMARY KEY,
	    data Date,
	    FK_CLIENTE_codigo integer
	);

	CREATE TABLE TIPO (
	    tipo varchar(30),
	    cod_tipo integer PRIMARY KEY
	);

	CREATE TABLE RAMO (
	    cod_ramo integer PRIMARY KEY,
	    ramo varchar(30)
	);

	CREATE TABLE AQUISICAO (
	    preco_aquisicao float,
	    codigo integer PRIMARY KEY,
	    data Date,
	    FK_FORNECEDOR_codigo integer
	);

	CREATE TABLE Itens (
	    fk_PRODUTO_codigo_produto integer,
	    fk_COMPRA_cod_compra integer,
	    qtd_venda integer,
	    cod_itens varchar(100) PRIMARY KEY
	);

	CREATE TABLE Pertence (
	    fk_FORNECEDOR_codigo integer,
	    fk_RAMO_cod_ramo integer
	);

	CREATE TABLE Produto_Aquisicao (
	    fk_PRODUTO_codigo_produto integer,
	    fk_AQUISICAO_codigo integer,
	    qtd_aquisicao integer,
	    cod varchar(100) PRIMARY KEY
	);

	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_2
	    FOREIGN KEY (FK_CATEGORIA_cod_categoria)
	    REFERENCES CATEGORIA (cod_categoria)
	    ON DELETE RESTRICT;

	ALTER TABLE CONTATO ADD CONSTRAINT FK_CONTATO_2
	    FOREIGN KEY (FK_FORNECEDOR_codigo)
	    REFERENCES FORNECEDOR (codigo)
	    ON DELETE RESTRICT;

	ALTER TABLE CONTATO ADD CONSTRAINT FK_CONTATO_3
	    FOREIGN KEY (FK_TIPO_cod_tipo)
	    REFERENCES TIPO (cod_tipo)
	    ON DELETE RESTRICT;

	ALTER TABLE COMPRA ADD CONSTRAINT FK_COMPRA_2
	    FOREIGN KEY (FK_CLIENTE_codigo)
	    REFERENCES CLIENTE (codigo)
	    ON DELETE CASCADE;

	ALTER TABLE AQUISICAO ADD CONSTRAINT FK_AQUISICAO_2
	    FOREIGN KEY (FK_FORNECEDOR_codigo)
	    REFERENCES FORNECEDOR (codigo)
	    ON DELETE RESTRICT;

	ALTER TABLE Itens ADD CONSTRAINT FK_Itens_2
	    FOREIGN KEY (fk_PRODUTO_codigo_produto)
	    REFERENCES PRODUTO (codigo_produto)
	    ON DELETE RESTRICT;

	ALTER TABLE Itens ADD CONSTRAINT FK_Itens_3
	    FOREIGN KEY (fk_COMPRA_cod_compra)
	    REFERENCES COMPRA (cod_compra)
	    ON DELETE SET NULL;

	ALTER TABLE Pertence ADD CONSTRAINT FK_Pertence_1
	    FOREIGN KEY (fk_FORNECEDOR_codigo)
	    REFERENCES FORNECEDOR (codigo)
	    ON DELETE RESTRICT;

	ALTER TABLE Pertence ADD CONSTRAINT FK_Pertence_2
	    FOREIGN KEY (fk_RAMO_cod_ramo)
	    REFERENCES RAMO (cod_ramo)
	    ON DELETE RESTRICT;

	ALTER TABLE Produto_Aquisicao ADD CONSTRAINT FK_Produto_Aquisicao_2
	    FOREIGN KEY (fk_PRODUTO_codigo_produto)
	    REFERENCES PRODUTO (codigo_produto)
	    ON DELETE RESTRICT;

	ALTER TABLE Produto_Aquisicao ADD CONSTRAINT FK_Produto_Aquisicao_3
	    FOREIGN KEY (fk_AQUISICAO_codigo)
	    REFERENCES AQUISICAO (codigo)
	    ON DELETE RESTRICT; 
	    
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        
	    INSERT INTO
		CLIENTE 
	VALUES ('Joana','F','1989-12-01',40.7143528,-73.0059731,1),
	('Gabriel','M','1982-11-08',40.7123528,-74.0159731,2),
	('Pedro','M','1981-06-08',40.7142528,-74.0039731,3),
	('Mariana','F','1970-05-09',40.7134548,-74.1159731,4),
	('Flávia','F','1990-04-09',40.7143524,-74.0099731,5),
	('Lucas','M','1985-02-09',40.7143520,-74.0088731,6),
	('Maria','F','1995-01-09',40.7143533,-74.0057731,7);



	INSERT INTO
		COMPRA
	VALUES (10,'2019-03-01',1),
	(20,'2019-04-02',2),
	(30,'2019-05-04',3),
	(40,'2019-08-05',4),
	(50,'2019-09-06',5),
	(60,'2019-06-08',6),
	(70,'2019-03-11',7);




	INSERT INTO
		CATEGORIA
	VALUES(11,'salto alto'),
	(22,'tênis'),
	(33,'meia'),
	(44,'sapatênis'),
	(55,'sapatilha'),
	(66,'sapato'),
	(77,'alpargata'),
	(88,'bota'),
	(99,'sandália');



	INSERT INTO
		PRODUTO
	VALUES(50,'Salto Preto',179.90,11),
	(100,'Salto Vermelho',149.90,11),
	(150,'Tênis Branco',159.90,22),
	(200,'Tênis Couro',169.90,22),
	(250,'Tênis Azul',179.90,22),
	(300,'Sapatênis',189.90,44),
	(350,'Meia branca',39.90,33),
	(400,'Meia preta',29.90,33),
	(450,'Sapatilha',49.90,55),
	(500,'Sapato Social Masculino',249.90,66),
	(550,'Alpargata',149.90,77),
	(600,'Bota Cano Curto',149.90,88),
	(650,'Bota Cano Longo',144.90,88),
	(700,'Salto Plataforma',159.90,11),
	(750,'Sandália',49.90,99);



	INSERT INTO
		FORNECEDO
	VALUES('Vizzano',111),
	('Puma',222),
	('Marianno',333),
	('Louis Vuitton',444),
	('Passarela',555),
	('Zanetti',666),
	('Bottero',777),
	('Dakota',888),
	('Ferricelli',999);


	INSERT INTO
		RAMO
	VALUES(11111,'sapatos'),
	(22222,'sapato esportivo'),
	(33333,'acessorios');



	INSERT INTO 
		TIPO
	VALUES('celular',1),('telefone',2),('e-mail',3);



	INSERT INTO
		CONTATO
	VALUES(21,'(11)1111-1111',111,1),
	(22,'(22)2222-2222',222,1),
	(23,'(33)3333-3333',333,1),
	(24,'(44)4444-4444',444,2),
	(30,'louisvuitton@gmail.com',444,3),
	(25,'(55)5555-5555',555,2),
	(26,'(66)6666-6666',666,1),
	(27,'(77)7777-7777',777,2),
	(28,'(88)8888-8888',888,2),
	(29,'(99)9999-9999',999,2);


	INSERT INTO
		AQUISICAO
	VALUES(19.0,101,'2019-01-01',111),
	(19.0,202,'2019-01-01',222),
	(19.0,303,'2019-01-01',222),
	(19.0,404,'2019-01-01',333),
	(19.0,505,'2019-01-01',444),
	(19.0,606,'2019-01-01',555),
	(19.0,707,'2019-01-01',666),
	(19.0,880,'2019-01-01',777),
	(69.0,878,'2019-01-01',888),
	(19.0,898,'2019-01-01',999),
	(39.0,858,'2019-01-01',777),
	(19.0,304,'2019-01-01',777),
	(29.0,838,'2019-01-01',777),
	(19.0,828,'2019-01-01',777),
	(19.0,818,'2019-01-01',777),
	(19.0,909,'2019-01-01',111);



	INSERT INTO 
		Pertence
	VALUES(111,11111),
	(222,22222),
	(222,33333),
	(333,11111),
	(444,11111),
	(555,11111),
	(666,11111),
	(777,11111),
	(888,11111),
	(999,11111);


	INSERT INTO 
	Itens
	VALUES(100,10,2,001),
	(150,10,3,002),
	(200,20,1,003),
	(350,30,2,004),
	(400,40,4,005),
	(550,50,6,006),
	(600,60,1,007),
	(750,70,1,008),
	(700,70,5,009),
	(250,70,3,010);


	INSERT INTO Produto_Aqusicao
	 VALUES (50,101,50,001),
	(100,101,50,002),
	(150,202,50,003),
	(200,202,50,004),
	(250,202,50,005),
	(300,404,50,006),
	(350,303,50,007),
	(400,303,50,008),
	(450,505,50,009),
	(500,606,50,010),
	(550,707,50,011),
	(600,818,50,012),
	(650,828,50,013),
	(700,101,50,014),
	(750,909,50,015);
	
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>

	#ExecutadoCLIENTE
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(101):
	  x = randint(0,1)
	  if (x == 0):
	    nome = fake.name_male()
	    sex = 'M'
	  else:
	    nome = fake.name_female()
	    sex = 'F'

	  data_nascimento = fake.date(pattern="%Y-%m-%d", end_datetime=None)
	  lat = fake.latitude()
	  long = fake.longitude()
	  cod = i + 1
	  #print(nome,sex,data_nascimento,lat,long,cod)
	  insert_instruction = """insert into CLIENTE values (%s,%s,%s,%s,%s,%s)"""
	  insert_values = (nome,sex,data_nascimento,lat,long,cod)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  
	  #ExecutadoCATEGORIA
	cur.execute("start transaction")
	fake = faker.Faker()
	tipoProd = ["Categ1","Categ2", "Categ3", "Categ4","Categ5"]
	for i in range(5):
	  cod_categoria = i +1
	  tipo = tipoProd[i]

	  print(cod_categoria,tipo)
	  insert_instruction = """insert into CATEGORIA values (%s,%s)"""
	  insert_values = (cod_categoria,tipo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  #ExecutadoTIPO
	cur.execute("start transaction")
	t = ["T1","T2","T3","T4","T5"]
	#fake = faker.Faker()
	for i in range(4):
	    cod_tipo = i + 1
	    tipo = t[i]
    
	    print(tipo,cod_tipo)
	    insert_instruction = """insert into TIPO values (%s,%s)"""
	    insert_values = (tipo,cod_tipo)
	    cur.execute(insert_instruction, insert_values)
	    cur.execute("commit")
	    
	    #ExecutadoFORNECEDOR
	cur.execute("start transaction")
	f = ["MarianaShop","GabrielShop","RodolfoShop","AnaShop","CalebeShop","MateusShop","EsShop","RodoShop","AnaShop","CalShop"]
	fake = faker.Faker()
	for i in range(10):
	    codigo = i +1
	    nome = f[i]
	    print(codigo,nome)
	    insert_instruction = """insert into fornecedor values (%s,%s)"""
	    insert_values = (nome,codigo)
	    cur.execute(insert_instruction, insert_values)
	    cur.execute("commit")
	    
	    #ExecutadoCOMPRA
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(100):
	  cod = i + 10
	  data = fake.date(pattern="%Y-%m-%d", end_datetime=None)
	  fk_cod_Cliente = randint(1,101)
	  print(cod, data, fk_cod_Cliente)
	  insert_instruction = """insert into COMPRA values (%s,%s,%s)"""
	  insert_values = (cod,data, fk_cod_Cliente)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoPRODUTO
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(101):
	  cod_produto = i + 100
	  nome = "Produto"+ str(i+1)
	  preco = round(random.uniform(100, 1000),2)
	  fk_cod_categoria = randint(1,5)
	  print(cod_produto,nome,preco,fk_cod_categoria)
	  insert_instruction = """insert into PRODUTO values (%s,%s,%s,%s)"""
	  insert_values = (cod_produto,nome,preco,fk_cod_categoria)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoRAMO
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(30):
	  cod_ramo = i +1
	  ramo = "Ramo"+ str(i+1)
	  print(cod_ramo,ramo)
	  insert_instruction = """insert into Ramo values (%s,%s)"""
	  insert_values = (cod_ramo,ramo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoPERTENCE
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(1,11):
	  fk_cod_fornecedor = i
	  fk_cod_ramo = randint(1,30)
	  print(fk_cod_fornecedor,fk_cod_ramo)
	  insert_instruction = """insert into Pertence values (%s,%s)"""
	  insert_values = (fk_cod_fornecedor,fk_cod_ramo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")

	for x in range(10):
	  fk_cod_fornecedor = randint(1,10)
	  fk_cod_ramo = randint(1,30)
	  print(fk_cod_fornecedor,fk_cod_ramo)

	  insert_instruction = """insert into Pertence values (%s,%s)"""
	  insert_values = (fk_cod_fornecedor,fk_cod_ramo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  #ExecutadoCONTATO
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(10):
	  cod_contato = i +1
	  fk_fornecedor = i +1
	  contato =""
	  for x in range(9):
	    contato = contato + str(randint(1,9))
	    #fk_fornecedor = i +1
	    fk_tipo = randint(1,4)


	  print(cod_contato,contato,fk_fornecedor,fk_tipo)
	  insert_instruction = """insert into CONTATO values (%s,%s,%s,%s)"""
	  insert_values = (cod_contato,contato,fk_fornecedor,fk_tipo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoITENS
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(100):
	  fk_produto = i + 100
	  fk_compra = i + 10
	  qtd_venda = randint(1,50)
	  cod_itens = i+1


	  print(fk_produto,fk_compra,qtd_venda,cod_itens)
	  insert_instruction = """insert into Itens values (%s,%s,%s,%s)"""
	  insert_values = (fk_produto,fk_compra,qtd_venda,cod_itens)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoAQUISIÇÃO
	cur.execute("start transaction")
	fake = faker.Faker()

	for i in range(100):
	  preco_aquisicao = round(random.uniform(10, 100),2)
	  cod = i + 1
	  data = fake.date(pattern="%Y-%m-%d", end_datetime=None)
	  fk_fornecedor = randint(1,10)


	  print(preco_aquisicao,cod,data,fk_fornecedor)
	  insert_instruction = """insert into AQUISICAO values (%s,%s,%s,%s)"""
	  insert_values = (preco_aquisicao,cod,data,fk_fornecedor)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  #ExecutadoPRODUTO_AQUISIÇÃO
	cur.execute("start transaction")
	fake = faker.Faker()

	for i in range(100):
	  fk_produto = i + 100
	  fk_aquisicao = i + 1
	  qtd_aquisicao = randint(50,101)
	  cod = str(i+1)


	  print(fk_produto,fk_aquisicao,qtd_aquisicao,cod)
	  insert_instruction = """insert into Produto_Aquisicao values (%s,%s,%s,%s)"""
	  insert_values = (fk_produto,fk_aquisicao,qtd_aquisicao,cod)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  


  









  
	
##Junção

	   CREATE TABLE CLIENTE (
	    nome varchar(50),
	    sexo char,
	    data_nascimento Date,
	    latitude float,
	    longitude float,
	    codigo integer PRIMARY KEY
	);

	CREATE TABLE PRODUTO (
	    codigo_produto integer PRIMARY KEY,
	    nome varchar(50),
	    preco_venda float,
	    FK_CATEGORIA_cod_categoria integer
	);

	CREATE TABLE FORNECEDOR (
	    nome varchar(50),
	    codigo integer PRIMARY KEY
	);

	CREATE TABLE CONTATO (
	    codigo_contato integer PRIMARY KEY,
	    contato varchar(30),
	    FK_FORNECEDOR_codigo integer,
	    FK_TIPO_cod_tipo integer
	);

	CREATE TABLE CATEGORIA (
	    cod_categoria integer PRIMARY KEY,
	    tipo varchar(30)
	);

	CREATE TABLE COMPRA (
	    cod_compra integer PRIMARY KEY,
	    data Date,
	    FK_CLIENTE_codigo integer
	);

	CREATE TABLE TIPO (
	    tipo varchar(30),
	    cod_tipo integer PRIMARY KEY
	);

	CREATE TABLE RAMO (
	    cod_ramo integer PRIMARY KEY,
	    ramo varchar(30)
	);

	CREATE TABLE AQUISICAO (
	    preco_aquisicao float,
	    codigo integer PRIMARY KEY,
	    data Date,
	    FK_FORNECEDOR_codigo integer
	);

	CREATE TABLE Itens (
	    fk_PRODUTO_codigo_produto integer,
	    fk_COMPRA_cod_compra integer,
	    qtd_venda integer,
	    cod_itens varchar(100) PRIMARY KEY
	);

	CREATE TABLE Pertence (
	    fk_FORNECEDOR_codigo integer,
	    fk_RAMO_cod_ramo integer
	);

	CREATE TABLE Produto_Aquisicao (
	    fk_PRODUTO_codigo_produto integer,
	    fk_AQUISICAO_codigo integer,
	    qtd_aquisicao integer,
	    cod varchar(100) PRIMARY KEY
	);

	ALTER TABLE PRODUTO ADD CONSTRAINT FK_PRODUTO_2
	    FOREIGN KEY (FK_CATEGORIA_cod_categoria)
	    REFERENCES CATEGORIA (cod_categoria)
	    ON DELETE RESTRICT;

	ALTER TABLE CONTATO ADD CONSTRAINT FK_CONTATO_2
	    FOREIGN KEY (FK_FORNECEDOR_codigo)
	    REFERENCES FORNECEDOR (codigo)
	    ON DELETE RESTRICT;

	ALTER TABLE CONTATO ADD CONSTRAINT FK_CONTATO_3
	    FOREIGN KEY (FK_TIPO_cod_tipo)
	    REFERENCES TIPO (cod_tipo)
	    ON DELETE RESTRICT;

	ALTER TABLE COMPRA ADD CONSTRAINT FK_COMPRA_2
	    FOREIGN KEY (FK_CLIENTE_codigo)
	    REFERENCES CLIENTE (codigo)
	    ON DELETE CASCADE;

	ALTER TABLE AQUISICAO ADD CONSTRAINT FK_AQUISICAO_2
	    FOREIGN KEY (FK_FORNECEDOR_codigo)
	    REFERENCES FORNECEDOR (codigo)
	    ON DELETE RESTRICT;

	ALTER TABLE Itens ADD CONSTRAINT FK_Itens_2
	    FOREIGN KEY (fk_PRODUTO_codigo_produto)
	    REFERENCES PRODUTO (codigo_produto)
	    ON DELETE RESTRICT;

	ALTER TABLE Itens ADD CONSTRAINT FK_Itens_3
	    FOREIGN KEY (fk_COMPRA_cod_compra)
	    REFERENCES COMPRA (cod_compra)
	    ON DELETE SET NULL;

	ALTER TABLE Pertence ADD CONSTRAINT FK_Pertence_1
	    FOREIGN KEY (fk_FORNECEDOR_codigo)
	    REFERENCES FORNECEDOR (codigo)
	    ON DELETE RESTRICT;

	ALTER TABLE Pertence ADD CONSTRAINT FK_Pertence_2
	    FOREIGN KEY (fk_RAMO_cod_ramo)
	    REFERENCES RAMO (cod_ramo)
	    ON DELETE RESTRICT;

	ALTER TABLE Produto_Aquisicao ADD CONSTRAINT FK_Produto_Aquisicao_2
	    FOREIGN KEY (fk_PRODUTO_codigo_produto)
	    REFERENCES PRODUTO (codigo_produto)
	    ON DELETE RESTRICT;

	ALTER TABLE Produto_Aquisicao ADD CONSTRAINT FK_Produto_Aquisicao_3
	    FOREIGN KEY (fk_AQUISICAO_codigo)
	    REFERENCES AQUISICAO (codigo)
	    ON DELETE RESTRICT;

	  
	#ExecutadoCLIENTE
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(101):
	  x = randint(0,1)
	  if (x == 0):
	    nome = fake.name_male()
	    sex = 'M'
	  else:
	    nome = fake.name_female()
	    sex = 'F'

	  data_nascimento = fake.date(pattern="%Y-%m-%d", end_datetime=None)
	  lat = fake.latitude()
	  long = fake.longitude()
	  cod = i + 1
	  #print(nome,sex,data_nascimento,lat,long,cod)
	  insert_instruction = """insert into CLIENTE values (%s,%s,%s,%s,%s,%s)"""
	  insert_values = (nome,sex,data_nascimento,lat,long,cod)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  
	  #ExecutadoCATEGORIA
	cur.execute("start transaction")
	fake = faker.Faker()
	tipoProd = ["Categ1","Categ2", "Categ3", "Categ4","Categ5"]
	for i in range(5):
	  cod_categoria = i +1
	  tipo = tipoProd[i]

	  print(cod_categoria,tipo)
	  insert_instruction = """insert into CATEGORIA values (%s,%s)"""
	  insert_values = (cod_categoria,tipo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  #ExecutadoTIPO
	cur.execute("start transaction")
	t = ["T1","T2","T3","T4","T5"]
	#fake = faker.Faker()
	for i in range(4):
	    cod_tipo = i + 1
	    tipo = t[i]
    
	    print(tipo,cod_tipo)
	    insert_instruction = """insert into TIPO values (%s,%s)"""
	    insert_values = (tipo,cod_tipo)
	    cur.execute(insert_instruction, insert_values)
	    cur.execute("commit")
	    
	    #ExecutadoFORNECEDOR
	cur.execute("start transaction")
	f = ["MarianaShop","GabrielShop","RodolfoShop","AnaShop","CalebeShop","MateusShop","EsShop","RodoShop","AnaShop","CalShop"]
	fake = faker.Faker()
	for i in range(10):
	    codigo = i +1
	    nome = f[i]
	    print(codigo,nome)
	    insert_instruction = """insert into fornecedor values (%s,%s)"""
	    insert_values = (nome,codigo)
	    cur.execute(insert_instruction, insert_values)
	    cur.execute("commit")
	    
	    #ExecutadoCOMPRA
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(100):
	  cod = i + 10
	  data = fake.date(pattern="%Y-%m-%d", end_datetime=None)
	  fk_cod_Cliente = randint(1,101)
	  print(cod, data, fk_cod_Cliente)
	  insert_instruction = """insert into COMPRA values (%s,%s,%s)"""
	  insert_values = (cod,data, fk_cod_Cliente)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoPRODUTO
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(101):
	  cod_produto = i + 100
	  nome = "Produto"+ str(i+1)
	  preco = round(random.uniform(100, 1000),2)
	  fk_cod_categoria = randint(1,5)
	  print(cod_produto,nome,preco,fk_cod_categoria)
	  insert_instruction = """insert into PRODUTO values (%s,%s,%s,%s)"""
	  insert_values = (cod_produto,nome,preco,fk_cod_categoria)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoRAMO
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(30):
	  cod_ramo = i +1
	  ramo = "Ramo"+ str(i+1)
	  print(cod_ramo,ramo)
	  insert_instruction = """insert into Ramo values (%s,%s)"""
	  insert_values = (cod_ramo,ramo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoPERTENCE
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(1,11):
	  fk_cod_fornecedor = i
	  fk_cod_ramo = randint(1,30)
	  print(fk_cod_fornecedor,fk_cod_ramo)
	  insert_instruction = """insert into Pertence values (%s,%s)"""
	  insert_values = (fk_cod_fornecedor,fk_cod_ramo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")

	for x in range(10):
	  fk_cod_fornecedor = randint(1,10)
	  fk_cod_ramo = randint(1,30)
	  print(fk_cod_fornecedor,fk_cod_ramo)

	  insert_instruction = """insert into Pertence values (%s,%s)"""
	  insert_values = (fk_cod_fornecedor,fk_cod_ramo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  #ExecutadoCONTATO
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(10):
	  cod_contato = i +1
	  fk_fornecedor = i +1
	  contato =""
	  for x in range(9):
	    contato = contato + str(randint(1,9))
	    #fk_fornecedor = i +1
	    fk_tipo = randint(1,4)


	  print(cod_contato,contato,fk_fornecedor,fk_tipo)
	  insert_instruction = """insert into CONTATO values (%s,%s,%s,%s)"""
	  insert_values = (cod_contato,contato,fk_fornecedor,fk_tipo)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoITENS
	cur.execute("start transaction")
	fake = faker.Faker()
	for i in range(100):
	  fk_produto = i + 100
	  fk_compra = i + 10
	  qtd_venda = randint(1,50)
	  cod_itens = i+1


	  print(fk_produto,fk_compra,qtd_venda,cod_itens)
	  insert_instruction = """insert into Itens values (%s,%s,%s,%s)"""
	  insert_values = (fk_produto,fk_compra,qtd_venda,cod_itens)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
	  #ExecutadoAQUISIÇÃO
	cur.execute("start transaction")
	fake = faker.Faker()

	for i in range(100):
	  preco_aquisicao = round(random.uniform(10, 100),2)
	  cod = i + 1
	  data = fake.date(pattern="%Y-%m-%d", end_datetime=None)
	  fk_fornecedor = randint(1,10)


	  print(preco_aquisicao,cod,data,fk_fornecedor)
	  insert_instruction = """insert into AQUISICAO values (%s,%s,%s,%s)"""
	  insert_values = (preco_aquisicao,cod,data,fk_fornecedor)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  #ExecutadoPRODUTO_AQUISIÇÃO
	cur.execute("start transaction")
	fake = faker.Faker()

	for i in range(100):
	  fk_produto = i + 100
	  fk_aquisicao = i + 1
	  qtd_aquisicao = randint(50,101)
	  cod = str(i+1)


	  print(fk_produto,fk_aquisicao,qtd_aquisicao,cod)
	  insert_instruction = """insert into Produto_Aquisicao values (%s,%s,%s,%s)"""
	  insert_values = (fk_produto,fk_aquisicao,qtd_aquisicao,cod)
	  cur.execute(insert_instruction, insert_values)
	  cur.execute("commit")
	  
	  
## Marco de Entrega 08 em: (29/05/2019)<br>

### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/cliente.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/compra.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/itens.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/produto.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/categoria.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/produto_aquisicao.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/aquisicao.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/fornecedor.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/contato.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/tipo.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/ramo.PNG)
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/pertence.PNG)



#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
	select * from Cliente where codigo = 10;

	select * from Cliente where sexo = 'F';

	select data from Compra where cod_compra = 30; 

	select * from Itens where qtd_venda = 20;

#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
	
	select * from Produto as prod where preco_venda > 500.00 and preco_venda < 800.00 and fk_categoria_cod_categoria = 2;

	select nome as Nome ,fk_categoria_cod_categoria as CodigoCategoria from Produto as prod where codigo_produto = 108 or codigo_produto = 159;

	select count(fk_categoria_cod_categoria) from Produto where fk_categoria_cod_categoria = 3;

	select count(fk_categoria_cod_categoria) as ProdsCategorias1_2 from Produto where not fk_categoria_cod_categoria = 3 and not fk_categoria_cod_categoria = 4 and not fk_categoria_cod_categoria = 5;

	select codigo_contato as Codigo,fk_fornecedor_codigo as CodigoFornecedor from contato where contato = '321532396';

	select sum(preco_aquisicao) from aquisicao where fk_fornecedor_codigo = 3;

	select sum(qtd_aquisicao) as quabtidadea_aquisicao from produto_aquisicao where fk_produto_codigo_produto = 120;

	select count(fk_fornecedor_codigo) as Quantidade_Fornecedores_Ramo from pertence where fk_ramo_cod_ramo = 19;

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
	select comp.cod_compra from compra comp where extract(year from comp.data) >= 2010;


	select cl.nome, cl.data_nascimento from cliente cl where extract(year from cl.data_nascimento) <= 2001 and cl.nome like 'C%';


	select cl.nome, cl.data_nascimento from cliente cl where cl.nome ilike 'j%';

	select sum(aq.preco_aquisicao) from aquisicao aq where extract(year from aq.data) >= 2010 and extract(year from aq.data) <= 2019;


	select cl.codigo, cl.nome from cliente cl where extract(year from cl.data_nascimento) <=2007 and extract(year from cl.data_nascimento) >= 2002 and cl.sexo = 'F';

	select avg(2019-extract(year from cl.data_nascimento)) from cliente cl;


    
#### 9.5	ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
	update fornecedor set nome = 'CaioShop' where nome = 'EsShop';

	update contato set contato = '997755312' where codigo_contato = 10;

	delete from cliente where codigo = 101;


#### 9.6	CONSULTAS COM JUNÇÃO E ORDENAÇÃO (Mínimo 6)<br>

	select * from itens order by 3 DESC;

	select prod.codigo_produto, prod.nome, prod.preco_venda-aq.preco_aquisicao as lucro from produto  prod join produto_aquisicao pa on (prod.codigo_produto = pa.fk_PRODUTO_codigo_produto) join aquisicao aq on (aq.codigo = pa.fk_AQUISICAO_codigo) group by prod.codigo_produto, prod.nome, prod.preco_venda-aq.preco_aquisicao order by 1 ASC;


	select cl.nome, count(comp.fk_CLIENTE_codigo) from cliente cl join compra comp on (comp.fk_CLIENTE_codigo = cl.codigo) group by cl.nome;


### ATUALIZAÇÃO DA DOCUMENTAÇÃO DOS SLIDES PARA APRESENTAÇAO SEMESTRAL (Mínimo 6 e Máximo 10)<br>


#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>

	select cat.tipo, count(prod.fk_CATEGORIA_cod_categoria) from categoria cat join produto prod on (prod.fk_CATEGORIA_cod_categoria = cat.cod_categoria) group by cat.tipo;


	select cat.cod_categoria, sum(it.qtd_venda) as qtd_vendas, count(it.cod_itens) as qtd_itens_categ from itens it join produto prod on (prod.codigo_produto = it.fk_PRODUTO_codigo_produto) join categoria cat on (prod.fk_CATEGORIA_cod_categoria = cat.cod_categoria) group by cat.cod_categoria order by 2 DESC limit 1;


	select f.nome, count(codigo_produto) as qtd_produtos_fornecidos from fornecedor f join aquisicao aq on (f.codigo = aq.fk_FORNECEDOR_codigo) join produto_aquisicao pa on (aq.codigo = pa.fk_AQUISICAO_codigo) join produto prod on (prod.codigo_produto = pa.fk_PRODUTO_codigo_produto) group by f.nome order by 2 DESC;

#### 9.8	CONSULTAS COM LEFT E RIGHT JOIN (Mínimo 4)<br>
	select cl.nome, comp.cod_compra from compra comp right join cliente cl on (comp.fk_CLIENTE_codigo = cl.codigo) order by 1 ASC;

	select f.nome, aq.codigo from fornecedor f left join aquisicao aq on (f.codigo = aq.fk_FORNECEDOR_codigo);

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
	create view cont_prod_cat as select cat.tipo, count(prod.fk_CATEGORIA_cod_categoria) from categoria cat join produto prod on (prod.fk_CATEGORIA_cod_categoria = cat.cod_categoria) group by cat.tipo;

	select * from cont_prod_cat;


	create view soma_cod3 as select sum(preco_aquisicao) from aquisicao where fk_fornecedor_codigo = 3;

	select * from soma_cod3;


	create view cat_mais_vendida asselect cat.cod_categoria, sum(it.qtd_venda) as qtd_vendas, count(it.cod_itens) as qtd_itens_categ from  itens it join produto prod on (prod.codigo_produto = it.fk_PRODUTO_codigo_produto) join categoria cat on (prod.fk_CATEGORIA_cod_categoria = cat.cod_categoria) group by cat.cod_categoria order by 2 DESC limit 1;

	select * from cat_mais_vendida;


#### 9.10	SUBCONSULTAS (Mínimo 3)<br>
	SELECT C.tipo, AVG(P.preco_venda) as Media_PRECOS_VENDA FROM Categoria C INNER JOIN PRODUTO P ON (P.fk_categoria_cod_categoria = C.cod_categoria) WHERE C.cod_categoria IN (select distinct cod_categoria from Categoria)GROUP BY C.tipo;

	select nome, data_nascimento from cliente where data_nascimento = (select MAX(data_nascimento) from cliente);

	select nome, preco_venda from produto where preco_venda  = (select MAX(preco_venda) from produto);



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


        
        


    





