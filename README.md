# Learn-SQL

## SQL: Basic tables
1. `CREATE`, `INSERT`, `SELECT`
```
exec(`CREATE TABLE users (email TEXT, name TEXT)`);
exec(`INSERT INTO users (email, name) VALUES ('amir@example.com', 'Amir')`);
exec(`SELECT * FROM users`);
//[{email: 'amir@example.com', name: 'Amir'}]
```
- `exec` is a JS function 
- We can specify which columns we want when SELECT
- `SELECT *` will select all the columns
- Executing a `SELECT` always returns an array of objects

- Not like `SELECT`, `CREATE` and `INSERT` don't retrieve data (Same for `DELETE`, `ALTER`, `BEGIN`)

- Common convention: UPPERCASE for SQL keywords, lower_snake_case for tables and columns

## SQL: Basic column types
1. `TEXT` - string.
2. `INTEGER` - whole numbers. can be positive or negative
3. `REAL` - e.g. 5.17, 0.00002, 11. the same data type as the number type in JS.

```
exec(`CREATE TABLE cats (name TEXT, age INTEGER)`);
exec(`INSERT INTO cats (name, age) VALUES ('Ms. Fluff', 3)`);
exec(`SELECT * FROM cats`);

/// [{age: 3, name: 'Ms. Fluff'}]
```


*** 
- PostgreSQL has 42 general purpose data types
- e.g. currency, for IP addresses, for XML, and many more.
- having many data type can make it easier to ensure that the data is correct.

***
<br>

## SQL: Selecting columns
1. When we `SELECT` columns by name, only those columns are returned.
```
// Write a query that selects only the login_count column

exec(`CREATE TABLE users (name TEXT, login_count INTEGER)`);
exec(`INSERT INTO users (name, login_count) VALUES ('Amir', 1)`);
exec(`SELECT login_count from users`);

//[{login_count: 1}]

// can select multiple columns by separating the columns names with a comma.
```