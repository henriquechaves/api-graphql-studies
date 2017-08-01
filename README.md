# API GraphQL

Framework para trabalhar mais facilmente com aplicações transacionais em requisições mais ágeis.

É muito importante quando queremos fazer muitas requisições em um modelo rest todo desnormalizado, faz com que tenhamos n requisições ao mesmo tempo
caindo na armadilha do chamado 'request hell'.

obs.: Não importa se os serviços usam uma API REST ou uma API GraphQL. Na verdade, se o seu serviço é realmente simples, o GraphQL só adicionará complexidade, portanto, uma API REST simples pode ser até melhor.

* O que é?
* Que problemas resolve?
* Como criar um servidor GraphQL?

## Alguns benefícios do GraphQL sobre o REST.

## Flexibilidade

Você pode consultar o schema navegando através das relações entre os resources economizando requisições ao servidor.

## Desempenho

Retorne apenas o que precisa, e não um resource que contém todos os dados.

## GraphQL codebase contém o para construção de APIs GraphQL (CRUD, auth, advanced patterns, etc) 

## Application Structure

* `data/schema.graphql` - Is the file that resolve the Graphql schema.
* `src/server.js` - Entry point of the application. This file define the Hapi.js server and graphql-server-hapi. 
* `src/core` - This folder contains all helper files, like `src/core/config.js` and `src/core/schema.js`.
* `src/resource` - This folder contains the resources folders. Any resource must auto contain itself.
* `src/resource/resolver.js` - This file must load and merge all the resolver files under the resource folder.
* `src/resource/users` - This file contains the `user` resource and have 2 files inside `controller.js` that have an abstraction of the user CRUD and `resolver.js`. 

