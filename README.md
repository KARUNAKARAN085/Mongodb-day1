# MongoDB Day 1

For the following question write the corresponding MongoDB queries

1. Find all the information about each products

    > db.product.find();

2. Find the product price which are between 400 to 800

    > db.product.find({product_price: {$gt: 400, $lt: 800}});

3. Find the product price which are not between 400 to 600

    > db.product.find({product_price: {$not: {$gt: 400, $lt: 600}}});

4. List the four product which are greater than 500 in price

    > db.product.find({product_price: {$gt: 500}}).limit(4);

5. Find the product name and product material of each products

    > db.product.find({}, {product_name: 1, product_material: 1});

6. Find the product with a row id of 10

    > db.product.find({id: '10'});

7. Find only the product name and product material

    > db.product.find({}, {product_name: 1, product_material: 1, \_id: 0});

8.  Find all products which contain the value of soft in product material

    > db.product.find({product_material: /soft/i});

9.  Find products which contain product color indigo and product price 492.00

    > db.product.find({product_color: "indigo", product_price: 492.00});

10. Delete the products which product price value are 28

    > db.product.remove({product_price: 28});