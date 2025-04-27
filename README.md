
Nome do Sistema: Sistema de gerenciamento de estoque

Versão: 1.0

1 – Apresentação:
Esse sistema é a solução para organizar tudo de forma fácil e rápida! Sem mais planilhas, sem mais caos! Imagine um assistente digital, só que muito mais legal. Estamos construindo isso porque, quem quer lidar com entrada manual de dados hoje em dia? Isso resolve o problema de informações espalhadas e tempo perdido. Funcionalidades básicas? Fácil! Interface amigável, armazenamento de dados seguro e talvez até alguma automação legal no futuro

2 – Descrição do Projeto e Usuários:
Este sistema utiliza um banco de dados MySQL para armazenar informações sobre produtos, fornecedores, clientes, pedidos e fluxo de caixa. O acesso ao sistema é controlado por níveis de permissão, garantindo a segurança da informação. 

Os cadastros serão:
Produtos
Fornecedores
Clientes
Pedidos
Caixa

Usuários e Permissões
Gerente  Acesso total a todas as funcionalidades do sistema.
Equipe  Acesso a informações sobre produtos, pedidos e clientes.
Financeiro  Acesso a informações sobre fornecedores e fluxo de caixa.

3 – Requisitos Funcionais
EF001- Cadastro de produto: permitir o registro de novos produtos, incluindo nome, preço, qauntidade em estoque, descrição e outras informações relevantes


4 – Requisitos Não Funcionais
RNFO001 – Segurança: implementar um sistema robusto de controle de acesso, garantindo que apenas usuários autorizados possam acessar informações e funcionalidades especificas

5 – Observações Técnicas
Segurança: Node.js com Express.js
Banco de dados: MySql
Segurança: Backups diários e envio de relatórios para o gerente.
