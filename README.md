# README do Projeto de API Web

## Introdução
Projeto de API web **Sistema de Gerenciamento de Usuários**, desenvolvido para a disciplina **Programação para Web**. A API é uma ferramenta para gerenciar usuários, permitindo criar, editar, excluir e listar usuários através de endpoints RESTful.

## Funcionalidades
- **Login**: Permite que os usuários façam login no sistema.
- **Criação de Usuário**: Permite a criação de novos usuários no sistema.
- **Listagem de Usuários**: Permite listar todos os usuários cadastrados.
- **Edição de Usuário**: Permite editar informações de um usuário existente.
- **Exclusão de Usuário**: Permite excluir um usuário do sistema.

## Requisitos
- **Python 3.8+**: Linguagem de programação utilizada para desenvolver a API.
- **FastAPI**: Framework web utilizado para criar a API.
- **SQLAlchemy/SQLModel**: Biblioteca de ORM para interação com o banco de dados.
- **SQLite**: Banco de dados relacional utilizado.

### Instalação da API
1. Baixe o arquivo ZIP do projeto e descompacte-o em seu diretório de preferência.
2. Navegue até o diretório do projeto:
    ```sh
    cd caminho/do/diretorio/descompactado
    ```
3. Crie um ambiente virtual:
    ```sh
    python -m venv venv
    ```
4. Ative o ambiente virtual:
    - Windows:
        ```sh
        venv\Scripts\activate
        ```
    - Unix/MacOS:
        ```sh
        source venv/bin/activate
        ```
5. Instale as dependências do projeto:
    ```sh
    pip install -r requirements.txt
    ```

## Uso da API

### Endpoints
- **Login**:
  - **Endpoint**: `/api/token`
  - **Método**: `POST`
  - **Parâmetros**:
    - `username`: Nome de usuário
    - `password`: Senha
  - **Exemplo**:
    ```sh
    curl -X POST "http://127.0.0.1:8000/api/token" -H "Content-Type: application/json" -d '{"username":"seu-usuario","password":"sua-senha"}'
    ```

- **Criação de Usuário**:
  - **Endpoint**: `/api/users/`
  - **Método**: `POST`
  - **Parâmetros**:
    - `username`: Nome de usuário
    - `email`: Email do usuário
    - `password`: Senha
  - **Exemplo**:
    ```sh
    curl -X POST "http://127.0.0.1:8000/api/users/" -H "Content-Type: application/json" -d '{"username":"novo-usuario","email":"email@exemplo.com","password":"senha"}'
    ```

- **Listagem de Usuários**:
  - **Endpoint**: `/api/users/`
  - **Método**: `GET`
  - **Exemplo**:
    ```sh
    curl -X GET "http://127.0.0.1:8000/api/users/"
    ```

- **Edição de Usuário**:
  - **Endpoint**: `/api/users/{user_id}`
  - **Método**: `PUT`
  - **Parâmetros**:
    - `username`: Nome de usuário (opcional)
    - `email`: Email do usuário (opcional)
    - `password`: Senha (opcional)
  - **Exemplo**:
    ```sh
    curl -X PUT "http://127.0.0.1:8000/api/users/1" -H "Content-Type: application/json" -d '{"username":"usuario-editado","email":"email@editado.com"}'
    ```

- **Exclusão de Usuário**:
  - **Endpoint**: `/api/users/{user_id}`
  - **Método**: `DELETE`
  - **Exemplo**:
    ```sh
    curl -X DELETE "http://127.0.0.1:8000/api/users/1"
    ```

## Testes
- **Teste de Login**: Verifica se um usuário pode fazer login com credenciais válidas.
- **Teste de Criação de Usuário**: Verifica se um novo usuário pode ser criado com sucesso.
- **Teste de Exclusão de Usuário**: Verifica se um usuário pode ser excluído do sistema.

## Contribuição
- **Luis Fyllypy**: Desenvolvedor principal
