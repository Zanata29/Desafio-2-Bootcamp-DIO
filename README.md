# Desafio-2-Bootcamp-DIO

CREATE TABLE Cliente (
    ClienteID INT PRIMARY KEY,
    Nome VARCHAR(100),
    Telefone VARCHAR(15),
    Endereco VARCHAR(255)
);

INSERT INTO Cliente (ClienteID, Nome, Telefone, Endereco) VALUES
(1, 'João Silva', '11987654321', 'Rua das Flores, 123'),
(2, 'Maria Oliveira', '11965498765', 'Avenida Central, 456');

SELECT Nome FROM Cliente;

SELECT * FROM OrdemServico WHERE DataConclusao IS NOT NULL;

SELECT ServicoID, Quantidade * PrecoUnitario AS CustoTotal FROM Servico;

SELECT Nome FROM Funcionário ORDER BY Salario DESC;

SELECT ClienteID, COUNT(*) AS TotalOS
FROM OrdemServico
GROUP BY ClienteID
HAVING COUNT(*) > 3;

SELECT c.Nome, v.Placa, o.DataAbertura
FROM Cliente c
INNER JOIN Veiculo v ON c.ClienteID = v.ClienteID
INNER JOIN OrdemServico o ON v.VeiculoID = o.VeiculoID;

Objetivo
O objetivo é:
- Criar um esquema lógico para o banco de dados utilizando o modelo ER desenvolvido anteriormente.
- Implementar o esquema em SQL para criação e persistência dos dados.
- Elaborar queries SQL mais complexas para atender a perguntas específicas e explorar os dados de forma eficiente.

Estrutura do Banco de Dados
- Entidades Principais:- Cliente
- Veículo
- Serviço
- Ordem de Serviço
- Funcionário
- Peça

- Relacionamentos:- Cada cliente pode ter múltiplos veículos registrados.
- Veículos podem estar associados a várias ordens de serviço.
- Ordens de serviço podem incluir múltiplos serviços e peças.
- Funcionários estão vinculados às ordens de serviço que executam.


Modelo Lógico
O esquema lógico foi projetado com base no modelo ER, considerando:
- Chaves primárias para identificação única.
- Chaves estrangeiras para relacionar tabelas.
- Restrições como CHECK para validações de dados.

Scripts e Implementação
Criação do Esquema
O script de criação do banco de dados inclui:
- Definição de tabelas com chaves primárias e estrangeiras.
- Restrições para garantir a integridade dos dados.


