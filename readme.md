# TRABALHO 01:  Marketplace de Imoveis
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
Arthur Cremasco | arthurcremascoamaral7@gmail.com<br>
Bruno Mian Silva | brunomian5@gmail.com<br>
Thalison Vinicius | thalison.ver@gmail.com<br>
...<br>


### 2.MINI-MUNDO<br>

A busca por um novo imóvel é uma etapa importante na vida de qualquer pessoa. No entanto, esse processo pode muitas vezes ser moroso e custoso, envolvendo deslocamentos, ligações telefônicas não atendidas e falta de transparência. Felizmente, a tecnologia moderna está desempenhando um papel crucial na simplificação desse processo e na melhoria da experiência do cliente no mercado imobiliário.<br>

Para começar, os clientes agora podem se cadastrar em sistemas online que coletam informações pessoais, como nome e endereço, permitindo criar um perfil que atenda às suas necessidades específicas. A partir desse ponto, a pesquisa de imóveis torna-se mais eficiente, com recursos de filtragem que incluem localização desejada, tipo de imóvel, preço, quantidade de cômodos e banheiros, entre outros critérios. O sistema então apresenta uma lista de opções que correspondem às preferências do cliente.<br>

Além disso, essas plataformas oferecem informações detalhadas sobre opções de financiamento, fornecendo aos clientes uma visão clara das possibilidades de pagamento. Após encontrar a propriedade desejada, a cliente pode agendar uma visita diretamente pelo sistema, eliminando a necessidade de ligações telefônicas não atendidas e deslocamentos desnecessários. As informações sobre as visitas disponíveis são facilmente localizadas, e o agendamento pode ser feito de forma conveniente.<br>

Essa abordagem inovadora traz transparência, praticidade e eficiência para o processo de compra de imóveis. Os clientes podem tomar decisões mais informadas, economizar tempo e recursos, e sentir-se mais confiantes em relação à sua escolha de propriedade, eliminando preocupações com a falta de informações relevantes ou falta de profissionalismo por parte dos corretores. No final, a tecnologia está revolucionando a forma como as pessoas encontram e adquirem seus imóveis, tornando o processo mais acessível e amigável.<br>


### 3.PERGUNTAS A SEREM RESPONDIDAS<br>
#### 3.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes?
	* Informações detalhadas sobre as propriedades disponíveis, incluindo preço, localização, características do imóvel, metragem, número de quartos, banheiros, etc.
 
	* Informações sobre opções de financiamento e cálculos de pagamento, como parcelas mensais, entrada, taxa de juros, prazos, etc.
 
	* Disponibilidade de visitas às propriedades, incluindo datas e horários disponíveis.
 
	* Histórico de preços de imóveis na área desejada.
 
	* Avaliação de mercado de uma propriedade.
 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
	* Relatório de Propriedades Disponíveis: Lista de todas as propriedades que atendem aos critérios de pesquisa do cliente, incluindo detalhes como preço, localização, metragem e características do imóvel.
	
	* Relatório de Opções de Financiamento: Um resumo das opções de financiamento disponíveis para as propriedades de interesse, incluindo cálculos de pagamento mensal, entrada, taxa de juros e prazos.
	
	* Relatório de Disponibilidade de Visitas: Uma lista de datas e horários disponíveis para visitas às propriedades selecionadas, permitindo que o cliente agende visitas de maneira conveniente.
	
	* Relatório de Histórico de Preços: Um histórico de preços de imóveis na área desejada, mostrando tendências de preços ao longo do tempo.
	
	* Relatório de Avaliação de Mercado: Uma avaliação do valor de mercado de uma propriedade específica, com base em fatores como localização, tamanho, condição e comparação com propriedades semelhantes na região

    
### 5.MODELO CONCEITUAL<br>
        
![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/31f7836d-09e1-4cce-bd04-bd189377d7ff)

#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: Emanuel Hoffmann
    [Grupo02]: Rodolfo Luiz

#### 5.2 Descrição dos dados 
Vamos lá!

**Objeto:** PESSOA <br>
**Descrição:** Tabela que armazena as informações relativas a uma pessoa ou corretor.<br>
**Campos:**<br>
- **código:** Identificador único da pessoa.<br>
- **nome:** Nome da pessoa.<br>
- **endereço:** Endereço da pessoa.<br>
- **dt_nasc:** Data de nascimento da pessoa.<br>

---

**Objeto:** CLIENTE <br>
**Descrição:** Tabela que relaciona um cliente à tabela de PESSOA e armazena seu CPF.<br>
**Campos:**<br>
- **fk_pessoa:** Chave estrangeira referenciando a tabela PESSOA.<br>
- **cpf:** Número de CPF do cliente.<br>

---

**Objeto:** CORRETOR <br>
**Descrição:** Tabela que relaciona um corretor à tabela de PESSOA e armazena seu horário de trabalho e número CRECI.<br>
**Campos:**
- **fk_pessoa:** Chave estrangeira referenciando a tabela PESSOA.<br>
- **horario_entrada:** Horário de entrada do corretor.<br>
- **horario_saida:** Horário de saida do corretor.<br>
- **creci:** Número de registro do corretor no CRECI.<br>

---

**Objeto:** CONTATO <br>
**Descrição:** Tabela que armazena informações de contato, como email e telefone.<br>
**Campos:**<br>
- **codigo:** Identificador único do contato.<br>
- **email:** Endereço de email.<br>
- **telefone:** Número de telefone.<br>

---

**Objeto:** PESSOA_CONTATO <br>
**Descrição:** Tabela de associação entre PESSOA e CONTATO para registrar os contatos de uma pessoa.<br>
**Campos:**<br>
- **fk_pessoa:** Chave estrangeira referenciando a tabela PESSOA.<br>
- **fk_contato:** Chave estrangeira referenciando a tabela CONTATO.<br>

---

**Objeto:** IMOVEL <br>
**Descrição:** Tabela que armazena informações sobre imóveis disponíveis.<br>
**Campos:**<br>
- **codigo:** Identificador único do imóvel.<br>
- **tipo:** Tipo do imóvel.<br>
- **endereço:** Endereço do imóvel.<br>
- **preco:** Preço do imóvel.<br>
- **estado:** Estado do imóvel.<br>

---

**Objeto:** AGENDAMENTO <br>
**Descrição:** Tabela que registra os agendamentos entre cliente, corretor e imóvel.<br>
**Campos:**<br>
- **fk_cliente:** Chave estrangeira referenciando a tabela PESSOA para o cliente.<br>
- **fk_corretor:** Chave estrangeira referenciando a tabela PESSOA para o corretor.<br>
- **fk_imovel:** Chave estrangeira referenciando a tabela IMOVEL.<br>
- **hora:** Hora do agendamento.<br>
- **data:** Data do agendamento.<br>

---

**Objeto:** INFRAESTRUTURA <br>
**Descrição:** Tabela que descreve as características dos imóveis.<br>
**Campos:**<br>
- **codigo:** Identificador único da característica.<br>
- **caracteristica:** comodos, banheiros, vagas, lazer.<br>

---

**Objeto:** POSSUI <br>
**Descrição:** Tabela de associação entre IMOVEL e CARACTERISTICA para registrar as características de um imóvel.<br>
**Campos:**<br>
- **fk_imovel:** Chave estrangeira referenciando a tabela IMOVEL.<br>
- **fk_caracteristica:** Chave estrangeira referenciando a tabela CARACTERISTICA.<br>
- **qtd:** Quantidade da característica no imóvel.<br>

---

**Objeto:** PAGAMENTO <br>
**Descrição:** Tabela que descreve os tipos de pagamento disponíveis.<br>
**Campos:**<br>
- **codigo:** Identificador único do tipo de pagamento.<br>
- **tipo:** Descrição do tipo de pagamento.<br>

---

**Objeto:** NEGOCIA <br>
**Descrição:** Tabela que registra as negociações entre cliente, corretor, imóvel e tipo de pagamento.<br>
**Campos:**<br>
- **fk_cliente:** Chave estrangeira referenciando a tabela PESSOA para o cliente.<br>
- **fk_corretor:** Chave estrangeira referenciando a tabela PESSOA para o corretor.<br>
- **fk_imovel:** Chave estrangeira referenciando a tabela IMOVEL.<br>
- **fk_pagamento:** Chave estrangeira referenciando a tabela PAGAMENTO.<br>
- **data:** Data da negociação.<br>
  	

># Marco de Entrega 01: Do item 1 até o item 5.2 (5 PTS) <br> 

### 6	MODELO LÓGICO<br>
![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/7b5e1ac3-27f7-41d0-9f0b-9cf124f8d3e5)

### 7	MODELO FÍSICO<br>
	CREATE TABLE PESSOA (
		codigo INTEGER PRIMARY KEY,
		nome VARCHAR(255),
		endereco VARCHAR(255),
		dt_nasc DATE
    	);

	CREATE TABLE CLIENTE (
		fk_Pessoa INTEGER REFERENCES PESSOA(codigo),
		cpf VARCHAR(11)
    	);

	CREATE TABLE CORRETOR (
		fk_Pessoa INTEGER REFERENCES PESSOA(codigo),
		creci INTEGER,
		horario_entrada TIME,
		horario_saida TIME
	);

	CREATE TABLE CONTATO (
		codigo INTEGER PRIMARY KEY,
		email VARCHAR(100),
		telefone VARCHAR(13);
	);

	CREATE TABLE PESSOA_CONTATO (
		fk_pessoa INTEGER REFERENCES PESSOA(codigo),
		fk_contato INTEGER REFERENCES CONTATO(codigo)
	);

	CREATE TABLE IMOVEL (
		codigo INTEGER PRIMARY KEY,
		tipo VARCHAR(25),
		endereco VARCHAR(255),
		preco FLOAT,
		estado VARCHAR(15)
	);

	CREATE TABLE AGENDAMENTO (
		fk_Imovel INTEGER REFERENCES IMOVEL(Imovel),
		fk_Cliente INTEGER REFERENCES PESSOA(Pessoa),
		fk_Corretor INTEGER REFERENCES PESSOA(Pessoa),
		hora TIME,
		data DATE
	);

	CREATE TABLE INFRAESTRURURA (
		codigo INTEGER PRIMARY KEY,
		caracteristica VARCHAR(255)
	);

	CREATE TABLE POSSUI (
		fk_imovel INTEGER REFERENCES IMOVEL(codigo),
		fk_infraestrutura INTEGER REFERENCES INFRAESTRUTURA(codigo),
		qtd INTEGER
	);
	
	CREATE TABLE PAGAMENTO (
		codigo INTEGER PRIMARY KEY,
		tipo VARCHAR(255)
	);
	
	CREATE TABLE NEGOCIA (
		fk_cliente INTEGER REFERENCES PESSOA(codigo),
		fk_corretor INTEGER REFERENCES PESSOA(codigo),
		fk_imovel INTEGER REFERENCES PESSOA(codigo),
		fk_pagamento INTEGER REFERENCES PAGAMENTO(codigo),
		data DATE
	);


### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
	ALTER TABLE IMOVEL
	DROP COLUMN ESTADO;
	
	ALTER TABLE IMOVEL
	ADD CONDICAO VARCHAR;
	
	ALTER TABLE INFRAESTRUTURA
	DROP COLUMN CARACTERISTICA;
	
	ALTER TABLE INFRAESTRUTURA
	ADD PROPRIEDADE VARCHAR;

	INSERT INTO PESSOA (codigo, nome, endereco, dt_nasc) VALUES
		(1, 'João Silva', 'Rua A, 123', '1990-05-15'),
		(2, 'Maria Santos', 'Av B, 456', '1985-08-20'),
		(3, 'Carlos Oliveira', 'Rua C, 789', '1982-03-10'),
		(4, 'Ana Souza', 'Av D, 321', '1995-12-05'),
		(5, 'Pedro Rocha', 'Rua E, 567', '1988-07-25');
	
	INSERT INTO CORRETOR (fk_Pessoa, creci, horario_entrada, horario_saida) VALUES
		(1, 12345, '09:00:00', '18:00:00'),
		(3, 67890, '10:00:00', '17:30:00');
	
	INSERT INTO CLIENTE (fk_Pessoa, cpf) VALUES
		(2, '12345678901'),
		(4, '98765432109'),
		(5, '34567890123');
	
	INSERT INTO CONTATO (codigo, email, telefone) VALUES
		(1, 'joao.silva@email.com', '+55 123456789'),
		(2, 'maria.santos@email.com', '+55 987654321'),
		(3, 'carlos.oliveira@email.com', '+55 111223344'),
		(4, 'ana.souza@email.com', '+55 554433322'),
		(5, 'pedro.rocha@email.com', '+55 998877665');
	
	INSERT INTO PESSOA_CONTATO (fk_pessoa, fk_contato) VALUES
		(1, 1),
		(2, 2),
		(3, 3),
		(4, 4),
		(5, 5);
	
	INSERT INTO IMOVEL (codigo, tipo, endereco, preco, estado) VALUES
		(1, 'Casa', 'Rua F, 789', 250000.00, 'A venda'),
		(2, 'Apartamento', 'Av G, 456', 180000.00, 'A venda'),
		(3, 'Casa', 'Rua H, 123', 300000.00, 'A venda'),
		(4, 'Apartamento', 'Av I, 789', 200000.00, 'Vendido'),
		(5, 'Casa', 'Rua J, 456', 280000.00, 'A venda');
	
	INSERT INTO AGENDAMENTO (fk_Imovel, fk_Cliente, fk_Corretor, hora, data) VALUES
		(1, 2, 1, '10:00', '2023-11-15'),
		(2, 4, 3, '14:30', '2023-11-17'),
		(3, 5, 3, '11:00', '2023-11-16'),
		(4, 5, 1, '15:00', '2023-11-18'),
		(5, 2, 3, '09:30', '2023-11-19');
	
	INSERT INTO INFRAESTRUTURA (codigo, caracteristica) VALUES
		(1, 'Piscina'),
		(2, 'Garagem'),
		(3, 'Academia'),
		(4, 'Varanda'),
		(5, 'Jardim');
	
	INSERT INTO POSSUI (fk_imovel, fk_infraestrutura, qtd) VALUES
		(1, 2, 1),
		(2, 4, 1),
		(3, 1, 1),
		(4, 3, 1),
		(5, 2, 1);
	
	INSERT INTO PAGAMENTO (codigo, tipo) VALUES
		(1, 'Dinheiro'),
		(2, 'Financiamento'),
		(3, 'Transferência Bancária'),
		(4, 'Cheque'),
		(5, 'Cartão de Crédito');
	
	INSERT INTO NEGOCIA (fk_cliente, fk_corretor, fk_imovel, fk_pagamento, data) VALUES
		(2, 1, 1, 5, '2023-11-16'),
		(4, 3, 2, 2, '2023-11-18'),
		(5, 2, 3, 1, '2023-11-17'),
		(3, 1, 4, 3, '2023-11-19'),
		(1, 3, 5, 4, '2023-11-20');

	2) script deve ser incluso no template em um arquivo no formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    https://colab.research.google.com/drive/1uyCQHk16mCX3FwYYE9oBz0srjMWgMNf_?usp=sharing
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
	# Inserir dados na tabela PESSOA
	select = pd.read_sql_query("select * from PESSOA", conn)
	select
	
	# Inserir dados na tabela CLIENTE
	select = pd.read_sql_query("select * from CLIENTE", conn)
	select
	
	Tabela Corretor:
	# Inserir dados na tabela CORRETOR
	select = pd.read_sql_query("select * from CORRETOR", conn)
	select
	
	# Inserir dados na tabela CONTATO
	select = pd.read_sql_query("select * from CONTATO", conn)
	select

 	# Inserir dados na tabela PESSOA_CONTATO
	select = pd.read_sql_query("select * from PESSOA_CONTATO", conn)
	select

 	# Inserir dados na tabela PAGAMENTO
	select = pd.read_sql_query("select * from PAGAMENTO", conn)
	select
 
 	# Inserir dados na tabela IMOVEL
	select = pd.read_sql_query("select * from IMOVEL", conn)
	select

  	# Inserir dados na tabela INFRAESTRUTURA
	select = pd.read_sql_query("select * from INFRAESTRUTURA", conn)
	select

 	# Inserir dados na tabela POSSUI
	select = pd.read_sql_query("select * from POSSUI", conn)
	select

 	# Inserir dados na tabela NEGOCIA
	select = pd.read_sql_query("select * from NEGOCIA", conn)
	select

 	# Inserir dados na tabela AGENDAMENTO
	select = pd.read_sql_query("select * from AGENDAMENTO", conn)
	select

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
	Selecionar todos os imóveis à venda (estado = 'A venda') com preço superior a 200.000:
		SELECT * FROM IMOVEL WHERE estado = 'A venda' AND preco > 200000.00;
	
	Selecionar todas as infraestruturas que não são garagem:
		SELECT * FROM INFRAESTRUTURA WHERE caracteristica <> 'Garagem';
	
	Selecionar todas as casas à venda (estado = 'A venda'):
		SELECT * FROM IMOVEL WHERE tipo = 'Casa' AND estado = 'A venda';
	
	Selecionar todas as negociações onde o pagamento não foi feito em dinheiro:
		SELECT * FROM NEGOCIA WHERE fk_pagamento <> (SELECT codigo FROM PAGAMENTO WHERE tipo = 'Dinheiro');

#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not

	# Selecionar todas as pessoas que têm um endereço cadastrado e nasceram antes de 1990:
		consulta = pd.read_sql_query("SELECT * FROM PESSOA WHERE endereco IS NOT NULL AND EXTRACT(YEAR FROM dt_nasc) < 1990;", conn)
		consulta

 	# Selecionar todas as pessoas que têm um endereço cadastrado e nasceram antes de 1990:
		consulta = pd.read_sql_query("SELECT * FROM IMOVEL WHERE CONDICAO = 'A venda' AND preco > 250000;", conn)
		consulta

 	# Selecionar todas as negociações concluidas com pagamento em dinheiro ou por transferencia bancária
		consulta = pd.read_sql_query("SELECT * FROM NEGOCIA WHERE (fk_pagamento IN (SELECT codigo FROM PAGAMENTO WHERE tipo IN ('Dinheiro', 'Transferência Bancária')));", conn)
		consulta
	
 	# Selecionar todas as pessoas que têm um endereço cadastrado
		consulta = pd.read_sql_query("SELECT * FROM PESSOA WHERE endereco IS NOT NULL;", conn)
		consulta

  	# Selecionar todos os imóveis que não possuem infraestrutura de academia:
		consulta = pd.read_sql_query("SELECT * FROM IMOVEL WHERE codigo NOT IN (SELECT fk_imovel FROM POSSUI WHERE fk_infraestrutura IN (SELECT codigo FROM INFRAESTRUTURA WHERE propriedade = 'Academia'));", conn)
		consulta

    b) Criar no mínimo 3 consultas com operadores aritméticos 
    
	# Calcular o valor total pago em negociações considerando um imposto de 5%:
		consulta = pd.read_sql_query("SELECT SUM(preco) + SUM(preco * 0.05) AS valor_total_com_imposto FROM NEGOCIA JOIN IMOVEL ON NEGOCIA.fk_imovel = IMOVEL.codigo;", conn)
		consulta
	
	# Calcular o desconto de 20% no preço dos imóveis à venda e o novo preço com desconto:
		consulta = pd.read_sql_query("SELECT codigo, tipo, preco, preco * 0.20 AS desconto, preco - (preco * 0.20) AS preco_com_desconto FROM IMOVEL WHERE condicao = 'A venda';", conn)
		consulta
	
	# Calcular a diferença de preço entre o imóvel mais caro e o mais barato:
		consulta = pd.read_sql_query("SELECT MAX(preco) AS preco_maximo, MIN(preco) AS preco_minimo, MAX(preco) - MIN(preco) AS diferenca_preco FROM IMOVEL;", conn)
		consulta

    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

		consulta = pd.read_sql_query("SELECT nome AS nome_cliente FROM PESSOA;", conn)
		consulta
	
		consulta = pd.read_sql_query("SELECT p.nome, c.cpf FROM CLIENTE c JOIN PESSOA p ON c.fk_Pessoa = p.codigo;", conn)
		consulta
	
		consulta = pd.read_sql_query("SELECT endereco AS localizacao, preco * 0.9 AS preco_com_desconto FROM IMOVEL;", conn)
		consulta


#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
	# Imoveis do tipo apartamento, sendo maiúscula ou minuscula 
	result = pd.read_sql_query("SELECT * FROM IMOVEL WHERE tipo ILIKE 'Apartamento%';", conn)
 
 	# Pessoas que começam com o nome 'Maria':
  	result = pd.read_sql_query("SELECT * FROM PESSOA WHERE nome LIKE 'Maria%';", conn)
   
	# Imoveis com endereço começando com 'Av':
 	result = pd.read_sql_query("SELECT * FROM IMOVEL WHERE endereco LIKE 'Av%';", conn)
  
	# Cliente que contem CPF começando com '12':
 	result = pd.read_sql_query("SELECT * FROM CLIENTE WHERE cpf LIKE '12%';", conn)
  
	# Contatos que contem email terminando em '.com'
 	result = pd.read_sql_query("SELECT * FROM CONTATO WHERE email LIKE '%.com';", conn)
  
  	# Propriedades com que contem 'ci', sendo maiúscula ou minuscula
   	result = pd.read_sql_query("SELECT * FROM INFRAESTRUTURA WHERE PROPRIEDADE ILIKE '%ci%';", conn)
    
  	# Pessoas com nome contendo 'a':
   	result = pd.read_sql_query("SELECT * FROM PESSOA WHERE nome LIKE '%a%';", conn)
    
    	# extrai o numrero correspondente ao dia da semana cotando a partir de 0 - domingo
     	result = pd.read_sql_query("SELECT EXTRACT(DOW FROM data) AS dia_semana_negocia FROM NEGOCIA WHERE data = '2023-11-16'",conn)
      
	# extrai o nome correspondente ao dia da semana cotando a partir de 0 - domingo
	result = pd.read_sql_query("SELECT TO_CHAR(data, 'Day') AS nome_dia_semana_negocia FROM NEGOCIA WHERE data = '2023-11-18'",conn)

 	# Extrai os dias da semana de todos os agendamentos
	result = pd.read_sql_query(""" SELECT fk_imovel, fk_cliente, fk_corretor, EXTRACT(DOW FROM data) AS dia_semana 		FROM AGENDAMENTO """,conn)
 
	# seleciona linhas que contem a data 2023-11-17 
	result = pd.read_sql_query(""" SELECT * FROM AGENDAMENTO WHERE data = '2023-11-17'""",conn)
 
 	# Pessoas que nasceram no mes 8 (Agosto)
        result = pd.read_sql_query("""SELECT * FROM PESSOA WHERE EXTRACT(MONTH FROM dt_nasc""",conn) = 8
""",conn)

 
 


    b) Criar uma consulta para cada tipo de função data apresentada.
    



># Marco de Entrega 02: Do item 6. até o item 9.1 (5 PTS) <br>

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão

	cur.execute("DELETE FROM NEGOCIA WHERE fk_cliente = 3")

	# Excluir uma negociação em relação a um corretor
	cur.execute("DELETE FROM NEGOCIA WHERE fk_corretor = 2")
	
	# Excluir um contato e a relação com uma pessoa:
	cur.execute("DELETE FROM CONTATO WHERE codigo = 2;")
	
    b) Criar minimo 3 de atualização

	# Atualizar a característica de uma infraestrutura:
	cur.execute("UPDATE INFRAESTRUTURA SET propriedade = 'Área de serviço' WHERE codigo = 1;")
	
	# Atualizar o preço de um imóvel:
	cur.execute("UPDATE IMOVEL SET preco = 300000.00 WHERE codigo = 3;")
	
	#Atualizar o tipo de um imóvel para 'Casa':
	cur.execute("UPDATE IMOVEL SET tipo = 'Casa' WHERE codigo = 1;")

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
	result = pd.read_sql_query("""
		SELECT *
		FROM PESSOA
		INNER JOIN CLIENTE ON PESSOA.codigo = CLIENTE.fk_Pessoa
		INNER JOIN CORRETOR ON PESSOA.codigo = CORRETOR.fk_Pessoa
		INNER JOIN PESSOA_CONTATO ON PESSOA.codigo = PESSOA_CONTATO.fk_pessoa
		INNER JOIN CONTATO ON PESSOA_CONTATO.fk_contato = CONTATO.codigo
		INNER JOIN NEGOCIA ON PESSOA.codigo = NEGOCIA.fk_cliente
		INNER JOIN IMOVEL ON NEGOCIA.fk_imovel = IMOVEL.codigo
		WHERE PESSOA.codigo IN (1, 2)
		ORDER BY PESSOA.codigo;
		""",conn)
	result
	
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

	# Junção entre PESSOA, PESSOA_CONTATO e CONTATO:
	result = pd.read_sql_query("""
		SELECT PESSOA.codigo, PESSOA.nome, CONTATO.email
		FROM PESSOA
		INNER JOIN PESSOA_CONTATO ON PESSOA.codigo = PESSOA_CONTATO.fk_pessoa
		INNER JOIN CONTATO ON PESSOA_CONTATO.fk_contato = CONTATO.codigo;
		""",conn)
	result
	
	# Listar agendamentos e ordenar por data e hora em ordem crescente:
	result = pd.read_sql_query("""
		SELECT AGENDAMENTO.fk_Imovel, AGENDAMENTO.fk_Cliente, AGENDAMENTO.fk_Corretor, AGENDAMENTO.hora, AGENDAMENTO.data
		FROM AGENDAMENTO
		ORDER BY AGENDAMENTO.data ASC, AGENDAMENTO.hora ASC;
		""",conn)
	result
	
	# Listar infraestruturas, imóveis e ordenar por característica em ordem alfabética:
	result = pd.read_sql_query("""
		SELECT INFRAESTRUTURA.propriedade, IMOVEL.tipo
		FROM INFRAESTRUTURA
		INNER JOIN POSSUI ON INFRAESTRUTURA.codigo = POSSUI.fk_infraestrutura
		INNER JOIN IMOVEL ON POSSUI.fk_imovel = IMOVEL.codigo
		ORDER BY INFRAESTRUTURA.propriedade ASC;
		""",conn)
	result
	
	# Listar imóveis, infraestruturas e ordenar por preço do imóvel em ordem crescente:
	result = pd.read_sql_query("""
		SELECT IMOVEL.tipo, INFRAESTRUTURA.propriedade, IMOVEL.preco
		FROM IMOVEL
		INNER JOIN POSSUI ON IMOVEL.codigo = POSSUI.fk_imovel
		INNER JOIN INFRAESTRUTURA ON POSSUI.fk_infraestrutura = INFRAESTRUTURA.codigo
		ORDER BY IMOVEL.preco ASC;
		""",conn)
	result
	
	# Listar pessoas, clientes, negociações e ordenar por nome da pessoa em ordem alfabética:
	result = pd.read_sql_query("""
		SELECT PESSOA.nome, CLIENTE.cpf, NEGOCIA.data
		FROM PESSOA
		INNER JOIN CLIENTE ON PESSOA.codigo = CLIENTE.fk_Pessoa
		INNER JOIN NEGOCIA ON CLIENTE.fk_Pessoa = NEGOCIA.fk_cliente
		ORDER BY PESSOA.nome ASC;
		""",conn)
	result

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
	# Contagem de Negociações por Tipo de Imóvel:
   	result = pd.read_sql_query("""
		SELECT IMOVEL.tipo, COUNT(NEGOCIA.fk_imovel) AS total_negociacoes
		FROM IMOVEL, NEGOCIA
		WHERE IMOVEL.codigo = NEGOCIA.fk_imovel
		GROUP BY IMOVEL.tipo;
		""",conn)
	result
 
	# Média de Preços por Condição do Imóvel:
	result = pd.read_sql_query("""
		SELECT IMOVEL.condicao, AVG(IMOVEL.preco) AS media_preco
		FROM IMOVEL
		GROUP BY IMOVEL.condicao;
		""",conn)
	result

  	# Contagem de Negociações por Tipo de Pagamento:
 	result = pd.read_sql_query("""
		SELECT PAGAMENTO.tipo, COUNT(NEGOCIA.fk_pagamento) AS total_negociacoes
		FROM PAGAMENTO INNER JOIN NEGOCIA ON PAGAMENTO.codigo = NEGOCIA.fk_pagamento
		GROUP BY PAGAMENTO.tipo;
		""",conn)
	result

  	#Contagem de Agendamentos por Tipo de Imóvel e Data:
	result = pd.read_sql_query("""
		SELECT IMOVEL.tipo, AGENDAMENTO.data AS Data_Marcada, COUNT(AGENDAMENTO.fk_Imovel) AS total_agendamentos
		FROM AGENDAMENTO INNER JOIN IMOVEL ON AGENDAMENTO.fk_Imovel = IMOVEL.codigo
		GROUP BY IMOVEL.tipo, AGENDAMENTO.data;
		""",conn)
	result

	#Contagem de Pessoas (Corretores e Clientes):
 	result = pd.read_sql_query("""SELECT 'Total Pessoas' AS Categoria,
		    CASE
		        WHEN fk_Pessoa IN (SELECT fk_Pessoa FROM CORRETOR) THEN 'Corretor'
		        WHEN fk_Pessoa IN (SELECT fk_Pessoa FROM CLIENTE) THEN 'Cliente'
		        ELSE 'Outro'
		    END AS Tipo_Pessoa,
		    COUNT(DISTINCT fk_Pessoa) AS total_pessoas
		FROM
		    (
		        SELECT fk_Pessoa FROM CORRETOR
		        UNION
		        SELECT fk_Pessoa FROM CLIENTE
		    ) AS Pessoas
		GROUP BY
		    Tipo_Pessoa;
		""",conn)
	result
 
	# Contagem de Imóveis com Piscina por Tipo:
	 result = pd.read_sql_query("""
		SELECT
		    IMOVEL.tipo AS Tipo_Imovel,
		    COUNT(IMOVEL.codigo) AS total_imoveis_com_piscina
		FROM IMOVEL
		    INNER JOIN POSSUI ON IMOVEL.codigo = POSSUI.fk_imovel
		    INNER JOIN INFRAESTRUTURA ON POSSUI.fk_infraestrutura = INFRAESTRUTURA.codigo
		WHERE
		    INFRAESTRUTURA.propriedade = 'Piscina'
		GROUP BY
		    IMOVEL.tipo
		ORDER BY
		    Tipo_Imovel;
		""",conn)
	result

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 03: Do item 9.2 até o ítem 9.10 (10 PTS)<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 04: Itens 10 e 11 (20 PTS) <br>
<br>
<br>




### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
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
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


