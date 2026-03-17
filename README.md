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

curl -X POST http://localhost:8080/api/products -H "Content-Type: application/json" -d "{\"name\":\"Laptop\",\"category\":\"Electronics\",\"price\":999.99,\"quantity\":10}"

curl -X PUT http://localhost:8080/api/products/1 -H "Content-Type: application/json" -d "{\"name\":\"Laptop Pro\",\"category\":\"Electronics\",\"price\":1299.99,\"quantity\":5}"

curl -X DELETE http://localhost:8080/api/products/1

## Sample responses

GET all:
[{"id":1,"name":"Laptop","category":"Electronics","price":999.99,"quantity":10}]

GET by id:
{"id":1,"name":"Laptop","category":"Electronics","price":999.99,"quantity":10}

POST:
{"id":1,"name":"Laptop","category":"Electronics","price":999.99,"quantity":10}