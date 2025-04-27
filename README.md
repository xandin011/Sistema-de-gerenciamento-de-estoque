CREATE DATABASE IF NOT EXISTS Gerenciador_de_estoque;
USE Gerenciador_de_estoque;

CREATE TABLE fornecedor (
    id_fornecedor INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(255) NOT NULL,
    contato VARCHAR(255),
    endereco VARCHAR(255)
);

CREATE TABLE produtos (
    id_produto INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(255) NOT NULL,
    descricao TEXT,
    preco DECIMAL(10, 2) NOT NULL,
    quantidade_estoque INT NOT NULL,
    id_fornecedor INT,
    produtocol VARCHAR(45),
    FOREIGN KEY (id_fornecedor) REFERENCES fornecedor(id_fornecedor)
);

INSERT INTO fornecedor (nome, contato, endereco) VALUES
('Fornecedor A', 'contato_a@email.com', 'Endereço A'),
('Fornecedor B', 'contato_b@email.com', 'Endereço B'),
('Fornecedor C', 'contato_c@email.com', 'Endereço C'),
('Fornecedor D', 'contato_d@email.com', 'Endereço D'),
('Fornecedor E', 'contato_e@email.com', 'Endereço E');

INSERT INTO produtos (nome, descricao, preco, quantidade_estoque, id_fornecedor, produtocol) VALUES
('Produto 1', 'Descrição do produto 1', 10.99, 100, 1, 'coluna1'),
('Produto 2', 'Descrição do produto 2', 20.99, 50, 2, 'coluna2'),
('Produto 3', 'Descrição do produto 3', 5.99, 200, 1, 'coluna3'),
('Produto 4', 'Descrição do produto 4', 15.99, 75, 3, 'coluna4'),
('Produto 5', 'Descrição do produto 5', 8.99, 150, 2, 'coluna5');

SELECT * FROM fornecedor;
SELECT * FROM produtos;

SELECT * FROM produtos WHERE id_fornecedor = 1;
SELECT * FROM fornecedor WHERE nome LIKE '%Fornecedor A%';

DELETE FROM produtos WHERE id_produto = 5;
DELETE FROM fornecedor WHERE id_fornecedor = 4;
