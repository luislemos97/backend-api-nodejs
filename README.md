# API RESTful de Recomendações e Registros

Este projeto consiste em duas APIs RESTful desenvolvidas em Node.js para gerenciamento de recomendações e registros de usuários. As APIs utilizam o banco de dados MongoDB para armazenar e recuperar dados e foram construídos para serem robustos, seguros e facilmente expansíveis.

## Tecnologias Utilizadas
- Node.js :
- Express : Framework web para Node.js que facilita a construção de APIs robustas e escaláveis.
- MongoDB : Banco de dados NoSQL utilizado para armazenar dados de recomendações e registros de usuários.
- Mongoose : Biblioteca de modelagem de objetos MongoDB para Node.js. Facilita a comunicação com o MongoDB, permitindo a definição de esquemas e a execução de validações.
- node-restful : Extensão para Express e Mongoose que simplifica a criação de endpoints RESTful, permitindo a definição de métodos HTTP e manipulação de dados de forma eficiente.
- Lodash : Biblioteca JavaScript que fornece recursos para tarefas comuns de programação como manipulação de arrays, objetos, etc. Utilizada aqui para manipulação de erros e formatação de respostas.
- Regex : Expressões regulares são usadas para validação de entrada de dados, garantindo que os dados de entrada sigam o formato esperado.
- 
## Estrutura do Projeto

O projeto segue uma estrutura organizada para separar claramente as responsabilidades de cada componente:

```
/project-root
 ├── /models                      # Modelos Mongoose para MongoDB
 │   ├── recommendation.js        # Modelo para recomendações
 │   └── register.js              # Modelo para registros de usuários
 ├── /controllers                 # Controladores da API, contendo lógica de manipulação de dados
 │   ├── recommendationController.js  # Controlador para a API de Recomendações
 │   └── registerController.js        # Controlador para a API de Registros
 ├── /routes                      # Definição das rotas da API
 │   ├── recommendationRoutes.js  # Rotas para a API de Recomendações
 │   └── registerRoutes.js        # Rotas para a API de Registros
 ├── /utils                       # Utilitários e funções auxiliares
 │   └── errorHandler.js          # Funções para tratamento de erros
 ├── server.js                    # Arquivo principal do servidor
 └── package.json                 # Configurações e dependências do projeto

```


## Funcionalidades

##### API de Recomendações ( recommendation)

Esta API gerencia dados de recomendações, permitindo que os usuários criem, leiam, atualizem e excluam recomendações.

Endpoints Disponíveis:

- GET /recommendations: Retorna todas as recomendações.
- POST /recommendations: Crie uma nova recomendação.
- PUT /recommendations/:id: Atualiza uma recomendação existente.
- DELETE /recommendations/:id: Exclui uma recomendação.
  
##### Validações:

- fullName: Deve ter pelo menos duas palavras, cada uma começando com uma letra guardada.
- description: Máximo de 500 caracteres.
- stars: Campo obrigatório.

##### Tratamento de Erros:

- Erros são tratados e formatados em respostas JSON amigáveis ​​para o cliente.
- Erros de banco de dados são capturados e retornados com mensagens específicas.

  
 ## API de Registros ( register)
 
### Esta API gerencia registros de usuários, permitindo operações CRUD.

### Endpoints Disponíveis:

- GET /registers: Retorna todos
- POST /registers: Cria um novo reino
- PUT /registers/:id: Atualiza um
- DELETE /registers/:id: Exclui um registro de usuário.

##### Validações:

- fullName: Deve ter pelo menos duas palavras, cada uma começando com uma letra guardada.
- mail: Formato de e-mail válido é obrigatório.

##### Tratamento de Erros:

- Validações são realizadas antes de operações de poste put.
- Mensagens de erro são claras e específicas para facilitar a correção de dados pelo usuário.

## Configuração e Execução
##### Pré-requisitos
- Node.js : Certifique-se de ter o Node.js instalado (versão 12.x ou superior).
- MongoDB : Ter um servidor MongoDB rodando localmente ou remotamente.

