# Lesson 3: WHERE - Filtering Rows
In this lesson, I learned that the `WHERE` clause is used to filter rows in a table based on a condition. The basic structure is:
```sql
SELECT column_name
FROM table_name
WHERE condition;
```

`SELECT` controls which columns are returned and in what order, while `WHERE` controls which rows are included in the result.

I practiced filtering by **text**, **numeric**, and **date values**.

Text values must be written in quotes, such as:

```sql
SELECT name, city
FROM customers
WHERE city = 'London';
```

Numeric values do not use quotes, such as:

```sql
SELECT name, email
FROM customers
WHERE customer_id = 4;
```
Date values are also written in quotes, such as:

```sql
SELECT name, signup_date
FROM customers
WHERE signup_date > '2024-08-01';
```

I also learned that a query can return multiple rows, one row, or zero rows depending on how many records match the condition. A zero-row result is not an error - it simply means no data matched the filter.

I learned that filtering is not limited to exact equality. Real business questions often ask for values **greater than**, **less than**, **not equal to**, or **within a boundary**.

The comparison operators I learned are:

```sql
=   -- equal to
>   -- greater than
<   -- less than
>=  -- greater than or equal to
<=  -- less than or equal to
!=  -- not equal to
```

I practiced using these comparison operators in queries such as:

```sql
SELECT name, signup_date
FROM customers
WHERE signup_date >= '2024-09-01';
```

This returns customers who signed up on or after `2024-09-01`.

```sql
SELECT name, signup_date
FROM customers
WHERE signup_date <= '2024-07-08';
```

This returns customers who signed up before or on `2024-07-08`.

```sql
SELECT name, city
FROM customers
WHERE customer_id != 1;
```

This returns all customers except the one with `customer_id = 1`.

I also learned that real business questions often need more than one condition. SQL uses `AND` and `OR` to combine conditions.

`AND` makes the filter narrower because both conditions must be true:

```sql
SELECT name, city, signup_date
FROM customers
WHERE city = 'London' AND signup_date > '2024-06-01';
```

This returns only customers who are in London and signed up after `2024-06-01`.

`OR` makes the filter wider because only one condition must be true:

```sql
SELECT name, city
FROM customers
WHERE city = 'London' OR city = 'Manchester';
```

This returns customers who are from London or Manchester.





