# bank_de_dados_senac.-- Criando tabela de Clientes
CREATE TABLE Cliente (
    id_cliente INT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    cpf VARCHAR(14) UNIQUE NOT NULL,
    data_nascimento DATE,
    telefone VARCHAR(20),
    email VARCHAR(100)
);

-- Criando tabela de Funcionarios
CREATE TABLE Funcionarios (
    id_funcionario INT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    cargo VARCHAR(50),
    salario DECIMAL(10,2),
    data_admissao DATE
);

-- Criando tabela de Capital (relacionada ao Cliente)
CREATE TABLE Capital (
    id_capital INT PRIMARY KEY,
    id_cliente INT,
    saldo DECIMAL(12,2) DEFAULT 0,
    limite_credito DECIMAL(12,2) DEFAULT 0,
    tipo_conta VARCHAR(20),
    
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id_cliente)
);
