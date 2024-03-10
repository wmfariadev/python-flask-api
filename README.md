# API Rest em Python com Flask, SQLAlchemy e Postgres

Este projeto é uma API Restful desenvolvida em Python como linguagem de programação. O framework Flask foi utilizado para a construção do servidor, enquanto o SQLAlchemy é utilizado como ORM para interagir com o banco de dados Postgres.

## Instalação

1. Certifique-se de ter o Python instalado em sua máquina.
2. Clone este repositório.
3. Instale as dependencias
```bash
pip install Flask
pip install SQLAlchemy
pip install Flask-Migrate
```

## Execução

Para efetuar a `migration` do banco de dados, execute o seguinte comando:

```bash
flask db init
flask db migrate -m 'init'
flask db upgrade
```

Para iniciar o servidor, execute o seguinte comando:

```bash
python app.py
```

A API será iniciada e estará acessível em `http://localhost:8080`.

## Endpoints

### Listar todos os livros

- Método: `GET`
- Rota: `/books`
- Descrição: Retorna uma lista com todos os livros cadastrados.

### Listar um único livro

- Método: `GET`
- Rota: `/books/:bookId`
- Descrição: Retorna os detalhes de um único livro com base no ID fornecido.

### Salvar um livro

- Método: `POST`
- Rota: `/books`
- Descrição: Salva um novo livro no banco de dados.
- Parâmetros do corpo da requisição:
  - `title` (string): Título do livro.
  - `author` (string): Autor do livro.
  - `description` (string): Descrição do livro.

### Deletar um livro

- Método: `DELETE`
- Rota: `/books/:bookId`
- Descrição: Deleta um livro do banco de dados com base no ID fornecido.

### Atualizar um livro

- Método: `PATCH`
- Rota: `/books/:bookId`
- Descrição: Atualiza os detalhes de um único livro com base no ID fornecido.
- Parâmetros do corpo da requisição (opcionais):
  - `isReading` (boolean): Indica se o livro está sendo lido.
  - `isFavorite` (boolean): Indica se o livro é favorito.
  - `isFinished` (boolean): Indica se o livro foi concluído.

## Estrutura de Pastas
```
├── migrations/
├── models/
├── src/
│   └── book.py
├── server.ts
├── .gitignore
├── app.py
└── db.py
```

**Desenvolvido por [William Faria](https://github.com/wmfariadev)**
