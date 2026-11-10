# 📘 Assignment: FastAPI Persistence with SQLite

## 🎯 Objective

Estenda a API de livros criada com FastAPI para armazenar dados em um banco SQLite local. Pratique criação de tabelas, consultas SQL parametrizadas e integração entre persistência e endpoints CRUD.

## 📝 Tasks

### 🛠️ Initialize the SQLite database

#### Descrição
Configure um banco SQLite em arquivo para armazenar os livros da API, usando o módulo `sqlite3` da biblioteca padrão do Python.

#### Requisitos
O programa concluído deve:

- Criar ou abrir um arquivo de banco de dados SQLite local.
- Criar uma tabela `books` com identificador, título e autor.
- Garantir que o identificador seja único e que título e autor sejam obrigatórios.
- Inicializar o banco automaticamente quando a aplicação iniciar, sem apagar registros existentes.

### 🛠️ Connect CRUD endpoints to SQLite

#### Descrição
Substitua o armazenamento em memória da API por operações no banco de dados para que os endpoints trabalhem com os registros persistidos.

#### Requisitos
O programa concluído deve:

- Atualizar `GET /books` e `GET /books/{book_id}` para consultar os dados no SQLite.
- Atualizar `POST /books`, `PUT /books/{book_id}` e `DELETE /books/{book_id}` para criar, atualizar e remover registros no banco.
- Usar consultas SQL parametrizadas para inserir e consultar dados.
- Manter os status HTTP definidos na atividade anterior, incluindo `201` na criação, `204` na exclusão e `404` para registros inexistentes.
- Confirmar as alterações no banco para que sejam salvas no arquivo.

### 🛠️ Verify persistence across server restarts

#### Descrição
Teste a API para confirmar que os dados continuam disponíveis após encerrar e iniciar o servidor novamente.

#### Requisitos
O programa concluído deve:

- Criar um livro usando `POST /books` e confirmar que ele aparece nas consultas.
- Encerrar e reiniciar o servidor sem remover o arquivo de banco de dados.
- Confirmar que o livro continua disponível após a reinicialização.
- Verificar que a atualização, a exclusão e as respostas para identificadores inexistentes continuam funcionando.
