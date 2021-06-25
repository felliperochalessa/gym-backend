# Gym API Documentação
### Sistema de gerenciamento de academias que permite o controle das informações referentes aos alunos, usuários, exercícios, categorias dos exercícios, treinos, e muito mais.

## Entidades do sistema

```json
Alunos
Avaliação física
Endereços
Exercícios
Categorias
Fichas de Treinos
Usuários
```

## Funcionalidades de cada entidade
**Alunos:**
```
POST:
{
  "nome" : "Nome do Aluno",
  "dataNascimento" : "00/00/0000",
  "cpf" : "000.000.000-00",
  "numeroCelular" : "(00) 90000-0000",
  "email" : "emailAluno@gmail.com",
  "genero" : "gênero do aluno",
  "idEndereco" : "id do endereço"
}

GET : 
  - /alunos -> obtém todos os alunos inclusos no sistema
  - /alunos/genero/:genero -> obtém todos os alunos de um determinado gênero
  - /alunos/email/:email -> obtém os dados do aluno do email especificado

PUT: 
  - /alunos/:email_do_aluno -> altera os dados referentes ao 
    aluno do email especificado
  
DELETE: 
  - /alunos/:email_do_aluno -> exclui todos os dados do aluno 
    referente ao email especificado
  
  Observação: ao remover um aluno do sistema, seus dados referentes as avaliações, treinos, mensalidades 
  e matrículas em modalidades são igualmente removidos
```
