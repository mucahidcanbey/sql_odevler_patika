


# ![Image](https://r.resimlink.com/QvqbJzUg.png)

## SQL Ödev 1

<br>

1-) <strong>film </strong>tablosunda bulunan <strong>title</strong> ve <strong>description</strong> 
sütunlarındaki verileri sıralayınız.

<br>

```
SELECT title, description FROM film;
```
![Proje](images/1_madde.png)

<br>

2-) <strong>film</strong>  tablosunda bulunan tüm sütunlardaki verileri film uzunluğu <strong>(length)</strong>  60 dan büyük <strong>VE</strong>  75 ten küçük olma koşullarıyla sıralayınız.

<br>

```
SELECT * FROM film
WHERE length > 60 AND length < 75;
```

![Proje](images/2_madde.png)

<br>

3-)  <strong>film</strong> tablosunda bulunan tüm sütunlardaki verileri  <strong>rental_rate</strong> 0.99  <strong>VE</strong>  <strong>replacement_cost</strong> 12.99  <strong>VEYA</strong> 28.99 olma koşullarıyla sıralayınız.

<br>

```
SELECT * FROM film
WHERE rental_rate = 0.99 AND replacement_cost = 12.99 
OR replacement_cost = 28.99;
```

![Proje](images/3_madde.png)

<br>

4-) <strong>customer</strong> tablosunda bulunan <strong>first_name</strong> sütunundaki değeri 'Mary' olan müşterinin <strong>last_name</strong> sütunundaki değeri nedir?

<br>

```
SELECT last_name FROM customer
WHERE first_name = 'Mary';
```

![Proje](images/4_madde.png)

<br>

5-) <strong>film</strong>  tablosundaki <strong>uzunluğu(length)</strong>  50 ten büyük OLMAYIP aynı zamanda <strong>rental_rate</strong>  değeri 2.99 <strong>veya</strong>  4.99 OLMAYAN verileri sıralayınız.

<br>

```
SELECT * FROM film
WHERE length <= 50 
AND NOT (rental_rate = 2.99 OR rental_rate = 4.99);
```

![Proje](images/5_madde.png)
