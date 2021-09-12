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

- Common convention: UPPERCASE for SQL keywords, lower_snace_case for tables and columns