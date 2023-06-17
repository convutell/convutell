# API

A API é utilizada para realizar o gerenciamento da aplicação e é consumida pela aplicação front-end para facilitar a utilização da ferramenta.

Utilizamos o framework FastAPI para a construção da API e o MongoDB como banco de dados para persistência dos dados.

![Texto alternativo](../assets/tutorial/b-api.png)

## Projetos

Todos os scripts são realizados dentro de um projeto. O projeto é responsável por gerenciar uma ou várias consultas construídas em Python ou SQL. O projeto pode possuir conexões ou não, dependendo do tipo de projeto. Caso seja um script, ele não verificará conexão.

Para executar os projetos, eles precisam estar ativos, o que é indicado pelo campo **fl_actived** na documentação.
 
**URL:** /GetAllProjects                
**Método:** GET                 
**Parâmetros:** Nenhum      
**Resposta de Sucesso:** Lista de objetos ProjectModel representando os projetos cadastrados.

Exemplo de requisição:

```bash

[
  {
    "id_project": 1,
    "name_project": "Projeto 1",
    "dt_last_run": "2023-06-15T10:30:00",
    "fl_active": true,
    "connection_origin1": "origem1",
    "connection_origin2": "origem2"
  }
]

```


## Query (Queries)

A rota de Consultas (Queries) permite gerenciar operações específicas realizadas dentro de um projeto. Essa rota oferece endpoints para criar, recuperar, atualizar e excluir consultas.

Criar Consulta
Endpoint para criar uma nova consulta.

**URL:** /CreateQueries                 
**Método:** POST                    
**Parâmetros:** Nenhum              
**Corpo da Requisição:** Objeto QuerySaveModel   representando os dados da consulta a ser criada.                                   
**Resposta de Sucesso:** Retorna o objeto QuerySaveModel representando a consulta criada.     

### Obter Consulta por ID
Recupera uma consulta com base em um ID específico.

**URL:** /GetQueriesId/{id_query}               
**Método:** GET                 
**Parâmetros:** id_query - ID da consulta a ser recuperada.                                 
**Resposta de Sucesso:** Retorna o objeto QueryModel representando a consulta encontrada.   

### Obter Consultas por ID do Projeto

Recupera todas as consultas associadas a um projeto específico.

**URL:** /GetqueriesIdprojects/{id_project}                 
**Método:** GET                     
**Parâmetros:** id_project - ID do projeto para o qual as consultas devem ser recuperadas.      
**Resposta de Sucesso:** Retorna o objeto       QueryModel representando a consulta encontrada.                                                  
### Atualizar Consulta

Atualiza uma consulta existente com base em um ID específico.

**URL:** /UpdateQueries/{id_query}              
**Método:** PUT                             
**Parâmetros:** id_query - ID da consulta a ser atualizada.                             
**Corpo da Requisição:** Objeto QuerySaveModel representando os dados atualizados da consulta.                                      
Resposta de Sucesso: Retorna o objeto QueryModel representando a consulta atualizada.                                   
### Excluir Consulta

Exclui uma consulta existente com base em um ID específico.

**URL:** /DeleteQueries/{id_query}              
**Método:** DELETE                              
**Parâmetros:** id_query - ID da consulta a ser excluída.                                    
**Resposta de Sucesso:** Retorna um objeto contendo a mensagem "Consulta excluída com sucesso".                                     

Essas rotas permitem o gerenciamento completo das consultas, incluindo criação, recuperação, atualização e exclusão. Você pode utilizar essas informações para documentar a funcionalidade e os retornos dessas rotas na sua documentação.
