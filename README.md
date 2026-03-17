# spring-boot-exam

Name: Abdulla AlMahmood

A simple product inventory API built with Spring Boot. Data is stored in memory, so it resets every time the app restarts.

## How to run

mvn spring-boot:run

App runs on http://localhost:8080

## Endpoints

GET /api/products - get all products
GET /api/products/{id} - get a product by id
POST /api/products - create a new product
PUT /api/products/{id} - update a product
DELETE /api/products/{id} - delete a product

## curl commands

curl http://localhost:8080/api/products

curl http://localhost:8080/api/products/1

Invoke-WebRequest -Uri http://localhost:8080/api/products -Method POST -ContentType "application/json" -Body '{"name":"Laptop","category":"Electronics","price":999.99,"quantity":10}'

Invoke-WebRequest -Uri http://localhost:8080/api/products/1 -Method PUT -ContentType "application/json" -Body '{"name":"Laptop Pro","category":"Electronics","price":1299.99,"quantity":5}'

Invoke-WebRequest -Uri http://localhost:8080/api/products/1 -Method DELETE

## Sample responses

GET /api/products:
[{"id":1,"name":"Laptop","category":"Electronics","price":999.99,"quantity":10}]

GET /api/products/1:
{"id":1,"name":"Laptop","category":"Electronics","price":999.99,"quantity":10}

POST /api/products:
{"id":2,"name":"Laptop","category":"Electronics","price":999.99,"quantity":10}

PUT /api/products/1:
{"id":1,"name":"Laptop Pro","category":"Electronics","price":1299.99,"quantity":5}

DELETE /api/products/1:
204 No Content