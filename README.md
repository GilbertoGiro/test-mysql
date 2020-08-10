# Teste MySQL para Desenvolvedor

## Solução:
  SELECT  CONCAT(cliente.nome, ' ', cliente.sobrenome) as 'Cliente',
      casa.cor AS 'Cor da casa',
      bairro.nome AS 'Bairro',
      carro.modelo AS 'Carro'
  FROM cliente
  LEFT JOIN casa
    ON casa.fk_cliente = cliente.id_cliente
  LEFT JOIN bairro
    ON bairro.id_bairro = casa.fk_bairro
  LEFT JOIN carro
    ON carro.fk_cliente = cliente.id_cliente;

## Objetivo:
Fazer uma query que retorne o relatório abaixo:
- Todos os clientes, cor de suas casas, seus bairros, seus carros

## Requisitos:
- Utilizar o dump desse projeto
