# TRABALHO 01:  SmartSales
Trabalho desenvolvido durante a disciplina de Banco de Dados do Integrado

# Sumário

### 1. COMPONENTES<br>
Júlia Suzano Fraga: juliasufraga18@gmail.com<br>
Betriz Auer Mariano: biaauer03@gmai.com<br>

### 2.INTRODUÇÃO E MOTIVAÇAO<br>

> A empresa SmartSales visa auxiliar a gestão de compra e venda de produtos, desde miniempresas a grandes negócios. Sabe-se que é demandado muito tempo para listar, estocar e fazer o balanço financeiro de uma empresa, o que pode resultar em falhas e, consequentemente, prejuízos. Sendo assim, a SmartSales tem como objetivo servir de apoio para o empresário, a fim de agilizar certos processos e contribuir no aumento da lucratividade. Após o cadastro de informações, que podem ser feitos manualmente ou por meio de sensores no estoque físico o sistema gerará relatórios que atenderão aos interesses do cliente.
 

### 3.MINI-MUNDO Novo<br>

> O sistema proposto para a SmartSales conterá as informações aqui detalhadas. Inicialmente, serão cadastrados os fornecedores de produtos, que contém o código, nome, ramo e contato da empresa, para que os responsáveis pela gestão saibam onde estão aplicando seu dinheiro, quais os fornecedores mais frequentes e até mesmo o que costuma ter os produtos mais baratos. Em seguida, é cadastrada a compra de produtos de um fornecedor, indicando o código do produto, o nome, tipo, a quantidade comprada, o preço e data de compra. A partir dessas duas entidades, o sistema já está pronto para computar sua função principal: a saída de produtos da loja ou empresa, a partir da nota fiscal, que contém número identificador, data da venda, produtos vendidos e sua quantidade, e o desconto, se houver e o cliente para o qual o produto foi vendido. Já os clientes serão cadastrados quando realizarem a primeira compra e terão código, nome, sexo e idade. 


### 4.RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto consta o pdf com o rascunho da interface do nosso programa.  <br>

![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/menu%20incial%20SS.jpg?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para SmartSales](https://github.com/SS-SmartSales/trabalho01/blob/master/novo%20Mini%20Mundo.pdf?raw=true "Empresa Devcom")


#### 4.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
 
> Para que o programa seja iniciado, ele precisa dos seguintes relatórios:
* Informações dos fornecedores com código, nome, ramo e contato.
* Informação do produto com código, nome, fornecedor, data de compra, quantidade comprada, preço de compra, preço de venda. Caso seja a primeira vez que o produto seja comprado, ele será inserido à tabela dos produtos. Caso não, a quantidade será somada a já existente.
* Informação dos clientes, que serão cadastrados ao fazerem sua primeira compra, com código, nome, idade e sexo.
> Para que funcione, precisa dos seguintes relatórios:
* Venda (funciona como uma nota fiscal) contendo o número da nota, o código do produto, a quantidade vendida, o desconto, se houver e o cliente para o qual o produto foi vendido.
> Com esses relatórios, o sistema consegue responder às seguintes questões:
* Quantos e quais produtos estão em estoque e foram vendidos;
* Qual o produto menos e mais vendido;
* Quanto foi a despesa e o lucro com os produtos;
* Qual o público do alvo dos produtos;
* Em quando tempo o dono da empresa precisa repor os produtos no estoque.
 

#### 4.2 TABELA DE DADOS DO SISTEMA:

>A tabela aqui anexada contém os atributos do sistema SmartSales. Ela simula um relatório com todos os dados que serão armazenados.

    PRODUTOS: tabela que contém as informações de todos os produtos comercializados pela empresa.
    FORNECEDORES: tabela que contém as informações de todos os fornecedores da loja.
    COMPRA: tabela que contém as informações de todas as vendas em um certo período. É importante para calcular o lucro e o número de produtos vendidos.
    CLIENTE: tabela que contém as informações de todos os clientes da loja, cadastrados ao realizar a primeira compra na loja.
    
![Exemplo de Tabela de dados da SmartSales](https://github.com/SS-SmartSales/trabalho01/blob/master/nova%20PlanilhaSmartsSales%20%20em%20ods.ods?raw=true "Tabela - SmartSales")

### 5.MODELO CONCEITUAL<br>

> O modelo conceitual apresenta as entidades existentes no programa e os relacionamentos que elas possuem entre si.
    
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/modelo%20conceitual.png?raw=true "Modelo Conceitual")
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Lucas Tejada Fabres e Caio Simão Lessa]
    [Grupo02]: [Rodolfo Luiz de Oliveira e Gustavo Olmo Santana]

#### 5.2 DESCRIÇÃO DOS DADOS 
    
    Tabela Produto
    CODIGO: Campo que armazena os códigos de cada produto.
    PRODUTO: Campo que armazena os nomes de cada produto .
    FORNECEDOR: Campo que armazena o código dos fornecedores de cada produto.
    DATA_AQUISICAO: Campo que armazena as datas de compra dos produtos.
    QTD_ADQUIRIDA: Campo que armazena as quantidades de produto comprados de um fornecedor.
    PRECO_AQUISICAO: Campo que armazena os preços de compra de cada produto.
    PRECO_VENDA: Campo que armazena os preços de venda de cada produto.
    
    Tabela Vendas
    NUMERO_NOTA: Campo que armazena o código de identificação da nota fiscal emitida ao final da venda de produtos.
    CODIGO: Campo que armazena o código do produto vendido.
    DATA_COMPRA: Campo que armazena a data de venda do produto.
    
    Tabela Fornecedores
    CODIGO: Campo que armazena o Cadastro Nacional da Pessoa Jurídica de cada fornecedor.
    NOME: Campo que armazena o nome de cada empresa fornecedora.
    RAMO: Campo que armazena o tipo de mercadoria que a empresa produz.
    CONTATO: Campo que armazena o contato do fornecedor.
    
    Tabela Clientes
    CODIGO: Campo que armazena o código do cliente.
    NOME: Campo que armazena o nome do cliente cadastrado.
    IDADE: Campo que armazena a idade do cliente.
    SEXO: Campo que armazena o sexo do cliente.
    LATITUDE: Campo que armazena a latitude do cliente.
    LONGITUDE: Campo que armazena a longitude do cliente.

### 6	MODELO LÓGICO<br>

> Aqui consta o modelo lógico do trabalho realizado pelo grupo.
    
![Alt text](https://github.com/SS-SmartSales/trabalho01/blob/master/ModeloConceitual.png)

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


        
        


    





