# Banco de Dados 1 - Ricardo André

## Projeto 1: Sistema de Gerenciamento de Biblioteca

### Entidades Principais:

**Livro:**

ISBN (Identificador único) - Tipo: String |
Título - Tipo: String |
Autor - Referência a entidade Autor |
Ano de Publicação - Tipo: Data |
Editora - Tipo: String |
Gênero - Tipo: String |
Número de Páginas - Tipo: Integer

**Autor:**

ID (Identificador único) - Tipo: String |
Nome - Tipo: String |
Nacionalidade - Tipo: String |
Data de Nascimento - Tipo: Data |
Gênero - Tipo: String

**Usuário:**

ID (Identificador único) - Tipo: String |
Nome - Tipo: String |
Data de Nascimento - Tipo: Data |
Tipo (Aluno, Professor, etc.) - Tipo: String |
Matrícula (apenas para Aluno) - Tipo: String |
Curso (apenas para Aluno) - Tipo: String |
Departamento (apenas para Professor) - Tipo: String |
Número de Registro (apenas para Professor) - Tipo: String

**Empréstimo:**

ID (Identificador único) - Tipo: String |
Data de Empréstimo - Tipo: Data |
Data de Devolução Prevista - Tipo: Data |
Data de Devolução Real - Tipo: Data

### Relacionamentos:

**Relacionamento entre Livro -> Autor:**

Um livro pode ter um ou mais autores. (1:N) /
Um autor pode ter escrito um ou mais de um livro. (N:1)

**Relacionamento entre Usuário -> Empréstimo:**

Um usuário pode fazer nenhum ou alguns empréstimos. (0:N) /
Um empréstimo é realizado por um único usuário. (1:1)

**Relacionamento entre Livro, Empréstimo e Usuário:**

Um empréstimo envolve um ou mais livros. (N:M) /
Um usuário pode realizar zero ou mais empréstimos. (0:N) /
Um livro pode estar presente em zero ou mais empréstimos. (0:N)

## Projeto 2: Sistema de Gestão de Vendas Online

### Entidades Principais:

**Produto:**

ID (Identificador único) - Tipo: String |
Nome - Tipo: String |
Descrição - Tipo: String |
Preço - Tipo: Decimal |
Estoque - Tipo: Integer |
Categoria - Tipo: String |

**Cliente:**

ID (Identificador único) - Tipo: String |
Nome - Tipo: String |
Endereço - Tipo: String |
E-mail - Tipo: String |
Telefone - Tipo: String 

**Pedido:**

ID (Identificador único) - Tipo: String |
Data do Pedido - Tipo: Data |
Status - Tipo: String (em Processo, Enviado, Entregue, Recebido, etc.) 

### Relacionamentos:

**Relacionamento entre Produto -> Pedido:**

Um pedido pode conter um ou mais produtos. (N:M) /
Um produto pode estar presente em zero ou mais pedidos. (0:N)

**Relacionamento entre Cliente -> Pedido:**

Um cliente pode fazer zero ou mais pedidos. (0:N) /
Um pedido é realizado por um único cliente. (1:1)

## Projeto 3: Sistema de Gerenciamento de Escola

### Entidades Principais:

**Aluno:**

ID (Identificador único) - Tipo: String |
Nome - Tipo: String |
Data de Nascimento - Tipo: Data |
Endereço - Tipo: String | 
E-mail - Tipo: String | 
Telefone - Tipo: String |
Matrícula - Tipo: String

**Professor:**

ID (Identificador único) - Tipo: String |
Nome - Tipo: String |
Data de Nascimento - Tipo: Data |
Endereço - Tipo: String |
E-mail - Tipo: String |
Telefone - Tipo: String |
Departamento - Tipo: String

**Disciplina:**

ID (Identificador único) - Tipo: String |
Nome - Tipo: String |
Descrição - Tipo: String |
Carga Horária - Tipo: Integer
Horário - Tipo: Integer

**Turma:**

ID (Identificador único) - Tipo: String |
Ano Letivo - Tipo: String |
Período - Tipo: String (manhã, tarde, noite) |
Sala - Tipo: String |
Turno - Tipo: String

**Nota:**

ID (Identificador único) - Tipo: String |
Valor - Tipo: Decimal |
Data de Lançamento - Tipo: Data 

### Relacionamentos

**Relacionamento entre Aluno -> Turma:**

Um aluno pode estar matriculado em uma ou mais turmas. (N:M) /
Uma turma pode ter um ou mais alunos matriculados. (N:M)

**Relacionamento entre Professor -> Turma:**

Um professor pode lecionar em uma ou mais turmas. (N:M) /
Uma turma é lecionada por um ou mais professores. (N:M)

**Relacionamento entre Aluno -> Nota:**

Um aluno pode ter zero ou mais notas atribuídas. (0:N) /
Uma nota é atribuída a um único aluno. (1:N)

**Relacionamento entre Turma, Disciplina e Professor:**

Uma turma pode estar associada a uma ou mais disciplinas. (N:M) /
Uma disciplina pode estar presente em uma ou mais turmas. (N:M) /
Um professor pode ser responsável por uma ou mais disciplinas em uma turma. (N:M)
