# *Desafio*

## *Criar uma api rest para gerenciamento de produtos em uma loja virtual*

*Objetivo*: Criar uma api rest que permite cadastrar, editar, visualizar e excluir produtos de uma loja virtual

*Requisitos obrigatórios:*

- a api deve ser feita com nodejs e deve rodar na porta 3000
- usar eslint e prettier para manter o código padronizado
- a api deve ser disponibilizada no github
- o desenvolvimento deve seguir algo próximo do gitflow e do conventional commits
- o projeto deve ter um arquivo README.md explicando o projeto e ensinando a realizar as instalações

### *Fase 1*

*Objetivo*: Criar um CRUD de produtos

*R1.1* - Um produto deve ter como propriedade:

- Código do Produto
- Nome
- Preço
- Informações do Produto
- Vendido por...
- Entregue por...

*R1.2* - Nunca deve existir dois produtos com a propriedade "Código do produto" repetida. (Cada produto deve ter seu código único)

*R1.3* - A api deve ter as seguintes rotas:

1. get: /produtos - deve retornar todos os produtos
2. post: /produtos - deve cadastrar um produto passado como parâmetro
3. put: /produtos/:codigo - deve alterar o produto no codigo escolhido para o produto passado como parâmetro
4. delete: /produtos/:codigo - deve deletar o produto no codigo escolhido

### *Fase 2*

Objetivo: Criar login de usuário e autenticação

*R2.1* - Neste passo, você deve incluir um usuário na api, que deve conter as seguintes propriedades:

- email
- senha

*R2.2* - A api deve incluir as seguintes rotas:

1. post: /cadastrar - deve receber um usuário e cadastrar no banco
1. post: /logar - deve receber um email e uma senha e retornar um token de acesso

*R2.3* - As apis de produto já cadastrada devem agora receber o token no header e só devem permitir realizar a operação caso o token seja válido. (O usuário está autenticado)

### *Fase 3*

*R3.1* O sistema deve incluir as seguintes rotas:

1. get: /produtos/:codigo - busca o produto com o código passado e retorna o produto, caso exista
1. get: /produtos/maiores-precos/:number - deve retornar os n produtos mais caros
1. get: /produtos/resumo - deve retornar uma lista com somente o nome e o preço de todos os produtos
1. get: /produtos/soma - deve retornar o valor da soma de todos os produtos cadastrados

### *Fase 4*

*R4.1* devem ser criados testes unitários para todo o sistema
*R4.2* devem ser criados testes funcionais para todas as rotas do sistema

### *Fase 5*

*R5.1* Os produtos agora devem ser salvos em um banco de dados
*R5.2* O sistema deve realizar logs em cada operação
*R5.3* O sistema deve conter um arquivo de configuração do Docker