# Store Api

Api made for furniture store with Node.js,Express.js,MongoDB & Mongoose

## Demo

https://user-images.githubusercontent.com/76695320/134520175-8c18c5e8-4106-4dec-b49e-4f28185cb7f4.mp4


## Screenshots

![image](https://user-images.githubusercontent.com/76695320/134512456-53d2cf76-ddf6-4110-b05e-6a15f03fcb23.png)

![image](https://user-images.githubusercontent.com/76695320/134516755-0ef17c78-4597-4689-b255-16e5571813e2.png)

![image](https://user-images.githubusercontent.com/76695320/134517103-6f048889-5a38-4921-869a-9be338355daa.png)

![image](https://user-images.githubusercontent.com/76695320/134517481-e25ae0e0-9dc4-4568-a407-9de07c5c5169.png)



## API Reference

#### Get all products

```http
  GET /api/v1/products
```

#### Get all products (based on filtering)

```http
  GET /api/v1/products?query=.......
```
#### Query

#### 1) name

| Query | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `name`      | `string` |  fetch similar pattern name|

#### 2) featured

| Query | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `featured`      | `boolean` |  fetch featured/non-featured products|

#### 3) company

| Query | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `company`      | `string` |  fetch products from company-list(ikea/caressa/liddy/marcos)|

#### 4) sort

| Query | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `sort`      | `string` |  sort products on any basis (eg: name -> ascending order / -name -> descending oder)|

#### 5) fields

| Query | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `fields`      | `string` |  fetch selected fields of products (eg : name,price)|

#### 6) limit

| Query | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `limit`      | `integer` |  limit the fetch quantity of products|

#### 7) page

| Query | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `page`      | `integer` |  fetch according to page|

#### 8) numericFilters

| Query | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `numericFilters`      | `conditions` |  fetch according to conditions (>,>=,=,<,<=) [eg: price>=40,rating>4.5]|


#### Get all products - testing

```http
  GET /api/v1/products/static
```


## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`MONGO_URI` = mongodb+srv://<your MongoDB access name>:<password>@nodeexpressprojects.50qvu.mongodb.net/myFirstDatabase?retryWrites=true&w=majority

`PORT` = port no you want to run in

## npm packages used

### dependensies

express

```http
  npm i express --save
```

mongoose

```http
  npm i mongoose
```

dotenv

```http
  npm i dotenv
```

### dev-dependensies

nodemon

```http
  npm i nodemon
```

## Run On Local-Machine

To startup nodemon

```http
  npm start
```

Manual start

```http
  node app.js
```

Explicit port initialization

```http
  PORT=<port-no> npm start
```

```http
  PORT=<port-no> node app.js
```
