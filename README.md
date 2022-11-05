# Postman + newman + github actions (Simple store template)


##  steps 
-  Download this repo.
-  Run `npm i` (install node.js dependencies)
-  Run `npm run tern-on-api`(to run testing server locally )

### Overview of server testing
Routes `/products`, `/orders` and `/users`. Below is a table of supported operations with `products` as example resource. The same operations are also supports for `orders/` and `users/`.

| VERB     |Route          | Input      | Output             |
|----------|---------------|------------|--------------------|
| GET      | /products     | *None*     | **Array**          |
| GET      | /products/:id |  **e.g 3** | **Object**         |
| POST     | /products     | **object** | **Created object** |
| PUT      | /products     | **object** | **Updated object** |
| DELETE   | /products/:id | **e.g 3**  | **Deleted object** |


- Upload `store.collection.json` in Postman app. (skip this exhibit in case you decide to use another public API ) 
- Make some integration tests in Postman, could be status code/JSON check and so on. ( in case with another API - write tests based on another one).

Examples:
- Test pagination, by way like `http://localhost:3000/users?page=1&pageSize=2`. 
- Test sorting, by way like `http://localhost:3000/users?sortOrder=ASC&sortKey=firstName`. You can sort an any resource response using query parameters sortOrder and sortKey.
-  Test status code for REST API (200,400 and so on).
-  Test response time.
-  Test response thanks to json schema validation.
-  Try to follow `AAA` approach (arrange, act, assert).

7. Save new collection with your new integration tests with the same name as `store.collection.json`. ( in case with another API - another file name for json file)
8. Push to you github repo in main branch ( in case with local server - save local server as well )

###  GH actions 


You can use another API to perform  your testing instead of local store API and `store.collection.json`. 
- <a href="https://github.com/public-apis/public-apis"> Public API list </a>

### Usefull links (skip this)
Examples with different actions in Postman workspace (only take a look once, no need to learn this) 
- <a href="https://www.postman.com/postman/workspace/postman-answers"> Postman answers </a>
- <a href="https://restfulapi.net"> REST API Tutorial </a>

Doc for json schema validation, to check output API response (only take a look once, no need to learn this doc) 
- <a href="https://json-schema.org"> json schema docs </a>
