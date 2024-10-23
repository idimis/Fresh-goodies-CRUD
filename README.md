Fresh Goodies API documentation that run on https://json-server-fresh-goodies.vercel.app/

Fresh Goodies CRUD
﻿

Product Test
﻿

GET
Get Product
https:\\json-server-fresh-goodies.vercel.app:443\products
Add description

·
﻿

GET
Get Product Ascending
https:\\json-server-fresh-goodies.vercel.app:443\products?_sort=name&_order=asc
Add description

·
﻿

Query Params
_sort
name
_order
asc
GET
Get Product Descending
https:\\json-server-fresh-goodies.vercel.app:443\products?_sort=name&_order=desc
Add description

·
﻿

Query Params
_sort
name
_order
desc
POST
Add Product
https:\\json-server-fresh-goodies.vercel.app:443\products
Add description

·
﻿

Body
raw (json)
View More
json
{
        "price": 0.0032,
        "weight": 1000,
        "name": "Beetles",
        "category": "Exotic",
        "imageUrl": "/products/beetles.png",
        "metadata": {
            "unit": "g",
            "weight": 100,
            "calorie": 190,
            "proteins": 24,
            "fats": 9,
            "increment": 100,
            "carbs": 2
        },
        "id": "999"
    }
PUT
Put Product
https:\\json-server-fresh-goodies.vercel.app:443\products\999
Add description

·
﻿

Body
raw (json)
View More
json
{
        "price": 0.0032,
        "weight": 1000,
        "name": "kucing",
        "category": "Exotic",
        "imageUrl": "/products/beetles.png",
        "metadata": {
            "unit": "g",
            "weight": 100,
            "calorie": 190,
            "proteins": 24,
            "fats": 9,
            "increment": 100,
            "carbs": 2
        },
        "id": "999"
    }
GET
Get Product
https:\\json-server-fresh-goodies.vercel.app:443\products\999
Add description

·
﻿

DELETE
Delete Product
https:\\json-server-fresh-goodies.vercel.app:443\products\999
Add description

·
﻿

Body
raw (json)
View More
json
{
        "price": 0.0032,
        "weight": 1000,
        "name": "Beetles",
        "category": "Exotic",
        "imageUrl": "/products/beetles.png",
        "metadata": {
            "unit": "g",
            "weight": 100,
            "calorie": 190,
            "proteins": 24,
            "fats": 9,
            "increment": 100,
            "carbs": 2
        },
        "id": "999"
    }
Cart Test
﻿

GET
Get Cart
https:\\json-server-fresh-goodies.vercel.app:443\cart
Add description

·
﻿

GET
Get One Cart
https:\\json-server-fresh-goodies.vercel.app:443\cart\100
Add description

·
﻿

DELETE
Delete Cart
https:\\json-server-fresh-goodies.vercel.app:443\cart\100
Add description

·
﻿

POST
Add Cart
https:\\json-server-fresh-goodies.vercel.app:443\cart
Add description

·
﻿

Body
raw (json)
json
{
        "id": "100",
        "productId": "0",
        "quantity": 12345679
    }
PUT
Put Cart
https:\\json-server-fresh-goodies.vercel.app:443\cart\100
Add description

·
﻿

Body
raw (json)
json
{
        "id": "100",
        "productId": "6",
        "quantity": 666
    }
Favorite Test
﻿

GET
Get Favorite
https:\\json-server-fresh-goodies.vercel.app:443\favorite-products
Add description

·
﻿

GET
Get One Favorite
https:\\json-server-fresh-goodies.vercel.app:443\favorite-products\999
Add description

·
﻿

DELETE
Delete One Favorite
https:\\json-server-fresh-goodies.vercel.app:443\favorite-products\999
Add description

·
﻿

POST
Add Favorite
https:\\json-server-fresh-goodies.vercel.app:443\favorite-products
Add description

·
﻿

Body
raw (json)
json
   {
        "productId": 0,
        "id": "999"
    }
PUT
Put Favorite
https:\\json-server-fresh-goodies.vercel.app:443\favorite-products\999
Add description

·
﻿

Body
raw (json)
json
   {
        "productId": 555,
        "id": "999"
    }

    