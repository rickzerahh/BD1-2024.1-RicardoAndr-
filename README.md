# Banco de Dados 1 - Ricardo André

![Sistema de Gerenciamento de Biblioteca](https://github.com/rickzerahh/BD1-2024.1-Ricardo_Andre-/assets/91620783/1400625c-1ed0-4641-a894-d6d9d5ff1940)

### Entidades Principais:

## Livro:

#### Chave Primária: ISBN

### Atributos:

Título ;

Ano de Publicação ;

Editora ;

Gênero ;

Número de Páginas.

## Autor:

#### Chave Primária: ID

### Atributos:

Nome ;

Nacionalidade ;

Data de Nascimento ;

Gênero.

## Usuário:

#### Chave Primária: ID

### Atributos:

Nome ;

Data de Nascimento ;

Tipo (Referência à entidade Aluno, Professor ou Outro).

## Empréstimo:

#### Chave Primária: ID

### Atributos:

Data de Empréstimo ;

Data de Devolução Prevista ;

Data de Devolução Real.

## Relacionamentos e Cardinalidades:

### Relacionamento entre Livro -> Autor:

Um livro pode ter um ou mais autores. (1:N) ;

Um autor pode ter escrito um ou mais livros. (N:1).

### Relacionamento entre Usuário -> Empréstimo:

Um usuário pode fazer zero ou mais empréstimos. (0:N) ;

Um empréstimo é realizado por um único usuário. (1:1).

### Relacionamento entre Livro, Empréstimo e Usuário:

Um empréstimo envolve um ou mais livros. (N:M) ;

Um usuário pode realizar zero ou mais empréstimos. (0:N) ;

Um livro pode estar presente em zero ou mais empréstimos. (0:N).

## Especialização-Generalização:

### Aluno:

Atributos adicionais: Matrícula, Curso

### Professor:

Atributos adicionais: Departamento, Número de Registro
