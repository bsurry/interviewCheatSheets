# SQL Basics Cheatsheet

## Creating Tables
```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100),
    created_at DATE
);
```

## Inserting Data
```sql
INSERT INTO users (id, name, email, created_at)
VALUES (1, 'Alice', 'alice@email.com', '2023-01-01');
```

## Selecting Data
```sql
SELECT * FROM users;
SELECT name, email FROM users WHERE id = 1;
```

## Updating Data
```sql
UPDATE users SET email = 'alice@newmail.com' WHERE id = 1;
```

## Deleting Data
```sql
DELETE FROM users WHERE id = 1;
```

## Filtering and Sorting
```sql
SELECT * FROM users WHERE name LIKE 'A%';
SELECT * FROM users ORDER BY created_at DESC;
```

## Aggregate Functions
```sql
SELECT COUNT(*) FROM users;
SELECT AVG(id) FROM users;
SELECT MIN(created_at), MAX(created_at) FROM users;
```

## Group By and Having
```sql
SELECT name, COUNT(*) FROM users GROUP BY name HAVING COUNT(*) > 1;
```

## Joins
```sql
SELECT u.name, o.amount
FROM users u
JOIN orders o ON u.id = o.user_id;
```

## Inner Join
```sql
SELECT users.name, orders.amount
FROM users
INNER JOIN orders ON users.id = orders.user_id;
```

## Left Outer Join
```sql
SELECT users.name, orders.amount
FROM users
LEFT OUTER JOIN orders ON users.id = orders.user_id;
```

## Right Outer Join
```sql
SELECT users.name, orders.amount
FROM users
RIGHT OUTER JOIN orders ON users.id = orders.user_id;
```

## Full Outer Join
```sql
SELECT users.name, orders.amount
FROM users
FULL OUTER JOIN orders ON users.id = orders.user_id;
```
