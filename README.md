------Descrição do Banco de Dados------

O banco de dados criado representa um sistema simples de uma instituição financeira fictícia chamada BancoDB. Ele foi projetado para armazenar informações essenciais sobre clientes, funcionários e o capital relacionado às contas bancárias. O banco possui três tabelas principais:

Cliente: Armazena dados dos clientes do banco, como nome, CPF, contato e data de nascimento.
Funcionarios: Guarda informações dos colaboradores da instituição, como nome, cargo, salário e data de admissão.
Capital: Contém os dados financeiros associados a cada cliente, incluindo saldo, limite de crédito e tipo de conta. Esta tabela possui uma chave estrangeira que se relaciona diretamente à tabela Cliente.


---

------Objetivo do Projeto e Aprendizado------

O objetivo deste projeto foi praticar e consolidar o uso dos comandos DDL (Data Definition Language) e DML (Data Manipulation Language) em SQL, criando um banco de dados do zero. Ao concluir o projeto, foi possível aprender a:

Planejar a estrutura de um banco de dados relacional.

Criar tabelas e definir seus relacionamentos.

Inserir, atualizar e excluir dados usando comandos SQL.

Alterar a estrutura de tabelas quando necessário.


Essas habilidades são fundamentais para a criação e manutenção de sistemas que dependem de armazenamento e manipulação de dados.


---

------Instruções para Executar o Script SQL------

1. Abra seu gerenciador de banco de dados (como MySQL Workbench, DBeaver, phpMyAdmin ou terminal MySQL).


2. Crie uma nova conexão com o servidor, caso ainda não exista.


3. Abra o arquivo bancodb.sql pelo editor da sua ferramenta.


4. Execute o script completo. Ele irá:

Criar o banco de dados BancoDB.

Criar as tabelas Cliente, Funcionarios e Capital.

Inserir dados de exemplo, se incluídos no script.

Demonstrar comandos de atualização e exclusão, caso aplicados.





---

------Comandos DDL e DML em SQL: O que são e como usar?------

Quando trabalhamos com bancos de dados relacionais, usamos SQL para estruturar e manipular informações. Os comandos SQL são divididos em dois grupos principais: DDL e DML.


---

------O que é DDL (Data Definition Language)?------

DDL significa "Linguagem de Definição de Dados". São comandos responsáveis por criar, modificar ou excluir estruturas do banco, como tabelas e bancos de dados.

Comandos DDL mais comuns

CREATE: Cria um banco de dados ou tabela.

ALTER: Altera a estrutura de uma tabela existente.

DROP: Remove uma tabela ou banco inteiro.


Exemplos práticos de DDL

Criar o banco:

CREATE DATABASE BancoDB;

Criar uma tabela:

CREATE TABLE Cliente (
   id_cliente INT PRIMARY KEY,
   nome VARCHAR(100),
   cpf VARCHAR(14)
);

Alterar uma tabela (adicionar coluna):

ALTER TABLE Funcionarios ADD telefone VARCHAR(20);


---

------O que é DML (Data Manipulation Language)?------

DML significa "Linguagem de Manipulação de Dados". Esses comandos são usados para inserir, consultar, atualizar e excluir registros das tabelas.

Comandos DML mais comuns

INSERT: Insere novos dados.

UPDATE: Atualiza registros existentes.

DELETE: Remove registros.

SELECT: Consulta os dados armazenados.


Exemplos práticos de DML

Inserir dados:

INSERT INTO Cliente (id_cliente, nome, cpf) 
VALUES (1, 'João Silva', '123.456.789-00');

Atualizar dados:

UPDATE Capital SET saldo = 1500.00 WHERE id_capital = 1;

Excluir dados:

DELETE FROM Funcionarios WHERE id_funcionario = 3;


---

------Resumindo------

DDL: Define a estrutura do banco (criação, alteração e exclusão de tabelas).

DML: Manipula os dados dentro das tabelas (inserção, atualização, exclusão e consulta).


Saber usar esses dois tipos de comandos é essencial para trabalhar com bancos de dados de forma eficiente.

Dica final: Pratique criando suas próprias tabelas e experimentando diferentes comandos. Isso ajuda a consolidar o aprendizado e a entender melhor o funcionamento de um banco relacional!
