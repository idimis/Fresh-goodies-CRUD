Fresh Goodies API documentation that run on https://json-server-fresh-goodies.vercel.app/

Base URL
Local:
arduino
Copy code
http://localhost:8080
Endpoints
1. Products
GET All Products (with optional sorting)
URL:

bash
Copy code
GET /products?_sort=name
Description:
Retrieves all products. You can sort the results by product name in ascending order.

Example Response:

json
Copy code
[
  {
    "id": 1,
    "price": 0.0032,
    "weight": 1000,
    "name": "Almonds",
    "category": "Nuts",
    "imageUrl": "/products/almonds.png",
    "metadata": {
      "unit": "g",
      "weight": 500,
      "calorie": 600,
      "proteins": 18
    }
  }
]
POST New Product
URL:
bash
Copy code
POST /products
Request Body:
json
Copy code
{
  "price": 0.005,
  "weight": 2000,
  "name": "Mangoes",
  "category": "Fruits",
  "imageUrl": "/products/mangoes.png",
  "metadata": {
    "unit": "kg",
    "weight": 2,
    "calorie": 200,
    "proteins": 2
  }
}
Response:
Status 201 Created.
PUT Update Product
URL:
bash
Copy code
PUT /products/1
Request Body:
json
Copy code
{
  "price": 0.006,
  "name": "Organic Mangoes"
}
Response:
Status 200 OK.
DELETE Product
URL:
bash
Copy code
DELETE /products/1
Response:
Status 200 OK.
2. Cart
GET All Cart Items
URL:
bash
Copy code
GET /cart
POST New Cart Item
URL:
bash
Copy code
POST /cart
Request Body:
json
Copy code
{
  "productId": 1,
  "quantity": 5
}
Response:
Status 201 Created.
PUT Update Cart Item
URL:
bash
Copy code
PUT /cart/1
Request Body:
json
Copy code
{
  "quantity": 10
}
Response:
Status 200 OK.
DELETE Cart Item
URL:
bash
Copy code
DELETE /cart/1
Response:
Status 200 OK.
3. Favorite Products
GET All Favorite Products
URL:
bash
Copy code
GET /favorite-products
POST New Favorite Product
URL:
bash
Copy code
POST /favorite-products
Request Body:
json
Copy code
{
  "productId": 2
}
Response:
Status 201 Created.
PUT Update Favorite Product
URL:
bash
Copy code
PUT /favorite-products/1
Request Body:
json
Copy code
{
  "productId": 3
}
Response:
Status 200 OK.
DELETE Favorite Product
URL:
bash
Copy code
DELETE /favorite-products/1
Response:
Status 200 OK.
Query Parameters for Sorting
You can use the _sort parameter with a GET request to sort data.

Usage
bash
Copy code
GET /products?_sort=name
Explanation:
This sorts the products by the name field in ascending order.

Optional Descending Sort:
To sort in descending order, add the _order query parameter:

sql
Copy code
GET /products?_sort=name&_order=desc
Environment Setup for Postman
To make your requests dynamic across environments (local and hosted):

Create Postman Environment Variables:

protocol: http
domain: localhost
port: 8080
product-address: products
cart-address: cart
favorite-product-address: favorite-products
Example Usage in Postman:

css
Copy code
{{protocol}}://{{domain}}:{{port}}/{{product-address}}