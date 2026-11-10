# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Desenvolva uma API REST para cadastrar e gerenciar livros usando FastAPI. Pratique rotas HTTP, validação de dados com Pydantic, operações CRUD e respostas de erro apropriadas.

## 📝 Tasks

### 🛠️ Create the FastAPI app and read endpoints

#### Descrição
Configure a aplicação FastAPI e crie endpoints para verificar se a API está ativa e consultar livros mantidos em memória.

#### Requisitos
O programa concluído deve:

- Criar uma instância `FastAPI` em `main.py` e iniciar o servidor com `uvicorn main:app --reload`.
- Implementar `GET /health`, retornando um status que indique que a API está ativa.
- Implementar `GET /books`, retornando a lista de livros disponíveis.
- Implementar `GET /books/{book_id}`, retornando o livro solicitado ou o status HTTP `404` quando ele não existir.

### 🛠️ Add and update books with validated data

#### Descrição
Defina o formato dos livros e implemente endpoints para adicionar e atualizar registros, validando os dados recebidos.

#### Requisitos
O programa concluído deve:

- Definir um modelo Pydantic para um livro, com título e autor obrigatórios.
- Implementar `POST /books` para validar e adicionar um livro, atribuindo-lhe um identificador único.
- Retornar o status HTTP `201` ao criar um livro.
- Implementar `PUT /books/{book_id}` para atualizar um livro existente.
- Retornar o status HTTP `404` ao tentar atualizar um livro inexistente.

### 🛠️ Delete books and verify the API

#### Descrição
Complete as operações da API removendo livros e verificando os endpoints e as respostas por meio da documentação automática do FastAPI.

#### Requisitos
O programa concluído deve:

- Implementar `DELETE /books/{book_id}` para remover um livro existente.
- Retornar o status HTTP `404` ao tentar remover um livro inexistente.
- Retornar o status HTTP `204` após remover um livro com sucesso.
- Permitir testar os endpoints pela interface `/docs` gerada pelo FastAPI.
- Manter os dados em memória e informar que eles são reiniciados quando o servidor é encerrado.
