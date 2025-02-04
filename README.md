# Desafio de Projeto: Refinando um Projeto Conceitual de Banco de Dados – E-COMMERCE

## Descrição do Projeto

Este projeto faz parte do "Desafio de Projeto: Refinando um Projeto Conceitual de Banco de Dados – E-COMMERCE". O objetivo é aprimorar um modelo conceitual de banco de dados para um sistema de e-commerce, aplicando boas práticas de modelagem e refinamento.

## Estrutura do Banco de Dados

O banco de dados foi modelado para atender às necessidades de um sistema de e-commerce, incluindo entidades como Cliente, Pedido, Forma de Pagamento, Entrega, entre outras. A estrutura foi projetada para ser flexível e eficiente, permitindo a gestão de clientes, pedidos, pagamentos e entregas de forma integrada.


## DESAFIO

"Refine o modelo apresentado acrescentando os seguintes pontos:
- Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
- Pagamento – Pode ter cadastrado mais de uma forma de pagamento;
- Entrega – Possui status e código de rastreio;"

## AÇÕES

- Implementado na entidade Cliente, o campo tipoCliente ENUM('PF', 'PJ'), fazendo com que o tipo seja definido na mesma tabela, se ele é pessoa física ou jurídica. Além disso, futuramente, implementarei algumas regras para que, ao escolher "PF", o campo Identificação permita apenas 11 caracteres, e se for escolhido "PJ", o campo permita 14 caracteres. Sobre a validação de DV, eu ainda não tenho conhecimento, mas irei me aprofundar nisso.

- Criada a entidade FormaPagamento, e relacionada em 1:n com clientes. No caso, um cliente pode ter várias formas de pagamento, e várias formas de pagamento podem compor a "carteira" do cliente. Essa nova entidade também foi relacionada à tabela Pedido, no caso de existir alguma forma de pagamento pontual relacionada diretamente ao pedido.

- Sobre a entrega, criei uma nova entidade para esse assunto e relacionei em 1:1 diretamente ao pedido. A rotina existente é que o pedido (pedido_idPedido) gera uma entrega (idEntrega) com as informações necessárias para um controle de entregas.


## Aprendizados

Foi extremamente gratificante aprender sobre diagramação e modelagem de banco de dados. Durante o desenvolvimento deste projeto, pude aprofundar meus conhecimentos em:

- Definição de relacionamentos entre entidades
- Implementação de triggers e constraints para garantir a integridade dos dados
- Melhoria contínua da estrutura do banco de dados

## Melhorias Futuras

Pretendo continuar aprimorando este projeto, implementando as seguintes melhorias:

- Ajustar regras para os campos, garantindo a validação correta dos dados inseridos
- Implementar medidas de segurança para proteger as informações sensíveis dos clientes
- Melhorar funcionalidades, como controle de estoque e consulta de vendas
- Otimizar consultas e índices para melhorar o desempenho do banco de dados


