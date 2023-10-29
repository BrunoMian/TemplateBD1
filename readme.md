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
        
![Alt text](https://github.com/BrunoMian/TemplateBD1/blob/3359981ac9c3e36b389c2a7d2b531da104187a7a/Modelo_Conceitual.jpg)
    
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: Emanuel Hoffmann
    [Grupo02]: Rodolfo Luiz

#### 5.2 Descrição dos dados 
	Objeto: PESSOA
	
	Descrição: Tabela que armazena as informações relativas a uma pessoa ou corretor.
	
	Campos:
	
	código: Identificador único da pessoa.
	nome: Nome da pessoa.
	endereço: Endereço da pessoa.
	telefone: Telefone da pessoa.
	email: Endereço de e-mail da pessoa.
 
	Objeto: CLIENTE
	
	Descrição: Tabela que armazena as informações relativas a uma pessoa.
	
	Campos:
	cpf: CPF da pessoa.

 	Objeto: CORRETOR
	
	Descrição: Tabela que armazena as informações relativas a um corretor.
	
	Campos:
	creci: certificado de corretor.
 	endereco: localização do corretor.
  	horario_trabalho: horario de atendimento.

	Objeto: IMÓVEL
	
	Descrição: Tabela que armazena as informações relativas a um imóvel.
	
	Campos:
	
	código: Identificador único do imóvel.
	tipo: Tipo de imóvel, como "casa", "apartamento", "terreno" ou "comercial".
	endereco: Endereço do imóvel.
	área: Área do imóvel.
	qtd_comodos: Número de quartos do imóvel.
	qtd_banheiros: Número de banheiros do imóvel.
	vagas de garagem: Número de vagas de garagem do imóvel.
	preco: Valor do imóvel.

	Objeto: AGENDAMENTO
	
	Descrição: relação que armazena as informações relativas ao agendamento de uma visita a um imóvel.
	
	Campos:
	
	codigo_agendamento: Identificador único do agendamento.
	tipo: Tipo de agendamento, como "visita", "contrato" ou "entrega".
	data: Data do agendamento.
	hora: Hora do agendamento.

	Relacionamentos:
	
	fk_codigo_cliente: Relacionamento com a tabela CLIENTE.
	fk_codigo_corretor: Relacionamento com a tabela CORRETOR.

 	Objeto: NEGOCIA
	
	Descrição: relação que armazena as informações da negociação do imovel.
	
	Campos:
 	data: Data da negociação.
  	metodo_pagamento: formas de pagamento.

 	codigo_agendamento:
	fk_codigo_cliente: Relacionamento com a tabela CLIENTE.
	fk_codigo_corretor: Relacionamento com a tabela CORRETOR.
  	

># Marco de Entrega 01: Do item 1 até o item 5.2 (5 PTS) <br> 

### 6	MODELO LÓGICO<br>
![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/aabcd84b-b71c-4bf3-8e01-46fc79fa4270)


### 7	MODELO FÍSICO<br>
	CREATE TABLE PESSOA (
 		codigoPessoa INTEGER PRIMARY KEY,
		nome VARCHAR,
   		telefone VARCHAR,
		endereco VARCHAR,
		dt_nasc DATE
  	);

	CREATE TABLE CLIENTE (
		fk_codigoPessoa INTEGER REFERENCES PESSOA,
		cpf VARCHAR
	);
 	
  	CREATE TABLE CORRETOR (
   		fk_codigoPessoa INTEGER REFERENCES PESSOA,
		creci INTEGER,
		horarioTrabalho TIME
  	);
   
   	CREATE TABLE IMOVEL (
		codigoImovel INTEGER PRIMARY KEY,
		tipo VARCHAR,
		endereco VARCHAR,
		preco FLOAT,
		qtd_comodos INTEGER,
		qtd_banheiros INTEGER,
		estado CHAR
  	);

	CREATE TABLE AGENDAMENTO (
		fk_codigoImovel INTEGER REFERENCES IMOVEL,
		fk_codigoCliente INTEGER REFERENCES PESSOA,
		fk_codigoCorretor INTEGER REFERENCES PESSOA,
		hora TIME,
		data DATE
  	);
   
   	CREATE TABLE NEGOCIA (
		fk_codigoCorretor INTEGER REFERENCES PESSOA,
		fk_codigoCliente INTEGER REFERENCES PESSOA,
		data DATE,
		metodoPagamento VARCHAR
  	);


### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
	ALTER TABLE CORRETOR
 	DROP COLUMN horarioTrabalho;

	ALTER TABLE CORRETOR
	ADD horarioEntrada TIME,
	ADD horarioSaida TIME;

	ALTER TABLE IMOVEL
	DROP COLUMN ESTADO;

	ALTER TABLE IMOVEL
	ADD ESTADO VARCHAR,

	INSERT INTO PESSOA (codigoPessoa, nome, telefone, endereco, dt_nasc)
	VALUES
	    (1, 'Bruno', '123-456-7890', 'Rua A, 1234', '1990-01-01'),
	    (2, 'Arthur', '987-654-3210', 'Rua B, 21', '1985-02-15'),
	    (3, 'Thalison', '555-555-5555', 'Rua C 114', '1988-07-20'),
	    (4, 'Maria', '111-222-3333', 'Rua D 121', '1995-03-10'),
	    (5, 'João', '222-333-4444', 'Rua E 235', '1977-12-05');

	INSERT INTO CLIENTE (fk_codigoPessoa, cpf)
	VALUES 
	    (1, '12345678901');
	    (3, '98765432109');
	    (4, '11122233344');
	
	INSERT INTO CORRETOR (fk_codigoPessoa, creci, horarioEntrada, horarioSaida)
	VALUES 
	    (5, '123456', '09:00:00', '18:00:00'),
	    (2, '789123', '08:00:00', '17:00:00');
	
	INSERT INTO IMOVEL (codigoImovel, tipo, endereco, preco, qtd_comodos, qtd_banheiros, estado)
	VALUES
	    (1, 'Casa', 'Rua A, 123', 250000.00, 4, 2, 'A venda'),
	    (2, 'Apartamento', 'Av. B, 456', 180000.00, 2, 1, 'A venda'),
	    (3, 'Casa', 'Rua C, 789', 350000.00, 5, 3, 'Vendido'),
	    (4, 'Apartamento', 'Av. D, 101', 200000.00, 3, 2, 'A venda'),
	    (5, 'Casa', 'Rua E, 111', 300000.00, 4, 2, 'A venda');
	
	INSERT INTO AGENDAMENTO (fk_codigoImovel, fk_codigoCliente, fk_codigoCorretor, hora, data)
	VALUES
	    (1, 3, 2, '10:00:00', '2023-10-25'),
	    (2, 1, 5, '14:30:00', '2023-10-26'),
	    (3, 4, 2, '11:15:00', '2023-10-27'),
	    (4, 4, 2, '15:00:00', '2023-10-28'),
	    (5, 1, 5, '13:45:00', '2023-10-29');

	INSERT INTO NEGOCIA (fk_codigoCorretor, fk_codigoCliente, data, metodoPagamento)
	VALUES
	    (2, 3, '2023-10-25', 'Financiamento'),
	    (5, 1, '2023-10-26', 'À vista'),
	    (2, 4, '2023-10-27', 'Financiamento'),
	    (2, 4, '2023-10-28', 'Cheque'),
	    (5, 1, '2023-10-29', 'Cartão de Crédito');


	2) script deve ser incluso no template em um arquivo no formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Usa template da disciplina disponibilizado no Colab.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
   Tabela Pessoa:
	
   ![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/97307b53-d683-46c9-82a5-df1aeacf050a)

   Tabela Cliente:
  	
   ![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/63a272be-bbe3-4be0-b415-d09716c12db3)
   
   Tabela Corretor:
    	
   ![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/0aae9206-c85b-4704-af25-978a06df9a64)

   Tabela Imovel:
      	
   ![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/897d074b-a0ce-4aca-af60-fcebb8f0a4fa)

   Tabela Agendamento:
	
   ![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/1ff1dfd4-cfea-4eff-884c-9042d380a68c)

   Tabela Negocia:
  	
   ![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/72798fa5-3f35-4415-b10f-b1204d65e312)

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/432a332d-4621-4cbf-8897-2b87589b1c9e)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/8a1ae591-3f0d-4dd6-9d71-26f1c7ee962f)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/ed3b2283-42c6-402f-a89f-14451edfcef3)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/6d93e52d-1278-4ae3-adbf-82c0d34d0d1c)

#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/6b41775f-f43c-471c-939a-fa6cc066f0ad)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/4c42e874-f7dd-46b2-8478-7a218dcae3b0)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/a827021a-e0a7-4dec-8523-664eea9e157f)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/19059161-8ee5-44a5-b250-f0c393d80f77)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/e6c3c35d-3994-4c41-baa4-cfd72e185ee5)
Consulta com operador AND para encontrar os agendamentos feitos por clientes 1 ou 3 com data posterior a '2023-10-26' e para imóveis à venda:
pd.read_sql_query("SELECT * FROM AGENDAMENTO WHERE (fk_codigoCliente = 1 OR fk_codigoCliente = 3) AND data > '2023-10-26' AND fk_codigoImovel IN (SELECT codigoImovel FROM IMOVEL WHERE estado = 'A venda')",conn)

    b) Criar no mínimo 3 consultas com operadores aritméticos 
![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/a97f81e7-3aca-499e-a68c-296ea79fee69)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/66d99cc6-d4bf-40c1-aaa4-6b1fbb425ece)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/eaddbb31-cd6b-4977-87e2-d4cb779dadff)

    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas
![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/ec662818-19f8-4f42-bd7a-b47493a5cfa3)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/4a301c8a-78ab-4cdf-bedc-5636c04b4b45)

![image](https://github.com/BrunoMian/TemplateBD1/assets/69252647/5304d85d-0021-4d99-a3f7-5146b0cb3b63)


#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/bf117e9a-c895-4d2e-a329-79edcc0b6a2d)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/8c44fd2e-da87-4b2f-a1b6-bbe980427aab)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/d469fe89-3b43-436c-b8d9-943d508529c4)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/fb700773-9b6c-42c6-a7dd-584999a1c41c)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/e71c880f-7ea4-49e3-b73a-710e22ec25f2)



    b) Criar uma consulta para cada tipo de função data apresentada.
    
![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/13995acd-0f7d-41fc-a2a4-715a64fb233f)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/d93437a4-c2c7-4efb-9d42-257d0a02b3d2)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/4a83d1e9-cc46-4f02-9b72-62ba03044761)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/822ba0b3-a48f-4084-a849-7a1f9978b4fa)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/e0df7945-d22a-4819-9f06-0a14d740419c)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/c83e8ac2-30c9-47b1-8b79-ac7d720ba56a)

![image](https://github.com/BrunoMian/TemplateBD1/assets/66493314/40dc9867-3b50-47b1-bcdd-f0bfb0df742f)


># Marco de Entrega 02: Do item 6. até o item 9.1 (5 PTS) <br>

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

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


