## Connect to DB

```sh
mysql -u $username -p $password -h $ip
```

- `show databases;` — Provides a list of available databases
- `use <database>;` — Navigates to the provided database
- `show tables;` — Provides a list of available tables within the database
- `show columns from <table>;` — Outputs columns of the provided table
- `select * from <table>;` — Outputs all contents of the provided table