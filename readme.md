# MongoDB Day 1

## 1.Find all the information about each products

```json

db.products.find()

```

![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

![alt text](image-3.png)

![alt text](image-4.png)

![alt text](image-5.png)

## 2.Find the product price which are between 400 to 800

```json

db.products.find({'product_price':{'$gte':400,'$lte':800}})

```

![alt text](image-6.png)

![alt text](image-7.png)

## 3.Find the product price which are not between 400 to 600

```json
db.products.find({'product_price':{'$not':{'$gte':400,'$lte':600}}})
```

![alt text](image-8.png)

![alt text](image-9.png)

![alt text](image-10.png)

![alt text](image-11.png)

![alt text](image-12.png)

![alt text](image-13.png)

## 4.List the four product which are greater than 500 in price

```json
db.products.find({},{product_name:1, product_material:1})

```

![alt text](image-14.png)

## 5.Find the product name and product material of each products

```json
db.products.find({},{product_name:1, product_material:1})
```

![alt text](image-20.png)

![alt text](image-21.png)

![alt text](image-22.png)

![alt text](image-23.png)

## 6.Find the product with a row id of 10

```json
db.products.find({id:"10"},{})
```

![alt text](image-19.png)

## 7.Find only the product name and product material

```json
db.products.find({}, {_id: 0, product_name: 1, product_material: 1})

```

![alt text](image-15.png)

![alt text](image-16.png)

![alt text](image-17.png)

![alt text](image-18.png)

## 8.Find all products which contain the value of soft in product material

```json
db.products.find({product_material: "Soft"})
```

![alt text](image-24.png)

![alt text](image-25.png)

## 9.Find products which contain product color indigo and product price 492.00

```json
db.products.find({ product_color: "indigo",product_price: 492.00})

```

![alt text](image-26.png)

## 10.Delete the products which product price value are 28

```json
db.products.deleteOne({product_price:28})
```

![alt text](image-27.png)
