## Create table

`CREATE TABLE products (`
`id SERIAL PRIMARY KEY,`
`name VARCHAR(50) NOT NULL,`
`department VARCHAR(50) NOT NULL,`
`price INTEGER NOT NULL DEFAULT 0 CHECK(price >=0),`
`WEIGHT INTEGER NOT NULL DEFAULT 0`
`)`

## Alter table

`ALTER TABLE products
ALTER price SET NOT NULL`

`ALTER TABLE products
ALTER weight DEFAULT 0`


`ALTER TABLE products
ADD UNIQUE(name)`

`ALTER TABLE products
ADD UNIQUE(name, department)`

`ALTER TABLE products 
DROP CONSTRAINT products_name_key`

`ALTER TABLE products 
ADD CHECK(price >=0)`

## Adding index
`create index on users(username)`
OR
`create index users_username_idx on users(username)`

## Droping index
`drop index users_username_idx `

## get execution time
`explain analyze select * from users where username='Emil30'`
