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

**Categorias:**
```
POST:
{
  "nome" : "Nome da Categoria",
}


GET : 
  - /categorias -> obtém todas as categorias inclusas no sistema

PUT: 
  - /categorias/:idCategoria -> altera os dados da categoria ao 
    informar o id da categoria correspondente. 
  
DELETE: 
  - /categorias/:idCategoria -> exclui os dados da categoria ao 
    informar o id da categoria correspondente.
    
    Observação: ao remover a categoria do sistema, qualquer exercício que utilize essa categoria 
    também é removido.
    
```

**Exercícios:**
```
POST:
{
  "nome" : "Nome do exercício",
  "descricao" : "descrição do exercício como os benefícios e para que serve",
  "idCategoria" : "id da categoria"
}


GET : 
  - /exercicios -> obtém todos os exercícios inclusos no sistema

PUT: 
  - /exercicios/:idExercicio -> altera os dados do exercício ao 
    informar o id do exercício correspondente. 
  
DELETE: 
  - /exercicios/:idExercicio -> exclui os dados do exercício ao 
    informar o id do exercício correspondente.
    
    Observação: ao remover o exercício do sistema, qualquer ficha de treino que utilize esse exercício 
    também é removida.
    
```
