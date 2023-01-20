# 2.SELECT

### 2.1: Selecting all columns

```sql
SELECT * FROM CUSTOMER;
```


To limit the number of records returned, use a LIMIT. To limit the results to just 2 records:

```sql
SELECT * FROM CUSTOMER LIMIT 2;
```

### 2.2: Selecting specific columns

```sql
SELECT CUSTOMER_ID, NAME FROM CUSTOMER;
```

### 2.3: Expressions

First, select everything from `PRODUCT`

```sql
SELECT * FROM PRODUCT;
```

You can use expressions by declaring a `TAXED_PRICE`. This is not a column, but rather something that is calculated every time this query is executed.

```sql
SELECT PRODUCT_ID,
DESCRIPTION,
PRICE,
PRICE * 1.07 AS TAXED_PRICE
FROM PRODUCT;
```

> In SQliteStudio, you can hit CTRL + SPACE on Windows and Linux to show an autocomplete box with available fields. For Mac, you will need to enable that configuration in preferences.

You can also use aliases to declare an `UNTAXED_PRICE` column off the `PRICE`, without any expression.

```sql
SELECT PRODUCT_ID,
DESCRIPTION,
PRICE as UNTAXED_PRICE,
PRICE * 1.07 AS TAXED_PRICE
FROM PRODUCT;
```

**SWITCH TO SLIDES** FOR MATHEMATICAL OPERATORS

### 2.4: Using `round()` Function

```sql
SELECT PRODUCT_ID,
DESCRIPTION,
PRICE,
round(PRICE * 1.07, 2) AS TAXED_PRICE

FROM PRODUCT;
```

### 2.5: Text Concatenation

You can slap a dollar sign to our result using concatenation.

```sql
SELECT PRODUCT_ID,
DESCRIPTION,
PRICE AS UNTAXED_PRICE,
'$' || round(PRICE * 1.07, 2) AS TAXED_PRICE
FROM PRODUCT
```

You can merge text via concatenation. For instance, you can concatenate two fields and put a comma and space ` ,` in between.

```sql
SELECT NAME,
CITY || ', ' || STATE AS LOCATION
FROM CUSTOMER;
```

You can concatenate several fields to create an address.

```sql
SELECT NAME,
STREET_ADDRESS || ' ' || CITY || ', ' || STATE || ' ' || ZIP AS SHIP_ADDRESS
FROM CUSTOMER;
```

This works with any data types, like numbers, texts, and dates. Also note that some platforms use `concat()` function instead of double pipes `||`

**SWITCH TO SLIDES** FOR EXERCISE


## 2.6: Comments

To make a comments in SQL, use commenting dashes or blocks:

```sql
-- this is a comment

/*
This is a
multiline comment
*/
```
