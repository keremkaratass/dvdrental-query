# SQL SORGULARI 

## Odev-1
```
SELECT title,description FROM film;
```

```
SELECT * FROM film
WHERE length>60 AND length<75;
```

```
SELECT * FROM film
WHERE (rental_rate=0.99 ) AND (replacement_cost=12.99 OR replacement_cost=28.99);
```

```
SELECT last_name FROM customer
WHERE first_name='Mary';
```

```
SELECT * FROM film
WHERE length<=50 AND NOT (rental_rate=2.99 OR rental_rate=4.99);
```
## Odev-2

```
SELECT * FROM film
WHERE replacement_cost BETWEEN 12.99 AND 16.99;
```

```
SELECT first_name,last_name FROM actor
WHERE first_name IN('Penelope','Nick','Ed');
```

```
SELECT * FROM film
WHERE (rental_rate IN(0.99,2.99,4.99)) AND (replacement_cost IN(12.99,15.99,28.99));
```

## Odev-3

```
SELECT country FROM country
WHERE country LIKE 'A%a';
```

```
SELECT country FROM country 
WHERE country LIKE '%_____a'; --Burda toplam 5 tane alt çizgi var
```

```
SELECT title FROM film
WHERE title ILIKE '%T%T%T%T%';
```

```
SELECT * FROM film
WHERE title LIKE 'C%' AND length>90 AND rental_rate=2.99;
```

## Odev-4

```
SELECT DISTINCT replacement_cost FROM film;
```

```
SELECT COUNT(DISTINCT replacement_cost) FROM film;
```

```
SELECT COUNT(*) FROM film 
WHERE title LIKE 'T%' AND rating='G';
```

```
SELECT COUNT(*) FROM country
WHERE country LIKE '_____';
```

```
SELECT COUNT(*) FROM city
WHERE city ILIKE '%r';
```

## Odev-5

```
SELECT title FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;
```

```
SELECT title,length FROM film
WHERE title LIKE '%n'
ORDER BY length ASC
OFFSET 5
LIMIT 5;
```

```
SELECT * FROM customer
WHERE store_id=1
ORDER BY last_name DESC 
LIMIT 4;
```