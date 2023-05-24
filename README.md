


# ![Image](https://r.resimlink.com/QvqbJzUg.png)

<br>
<br>
<br>

> #### Bu repo'da [Patika](https://academy.patika.dev/) SQL eğitiminde yapmış olduğunuz bütün ödevler bulunmaktadır.

<br>
<br>

 1. ####  <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-1--where-ve-kar%C5%9F%C4%B1la%C5%9Ft%C4%B1rma--mant%C4%B1ksal-operat%C3%B6rler">SQL Ödev 1 | </a>
 2. #### <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-2--between-ve-in">SQL Ödev 2 | </a>
 3. ####  <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-3--like-ve-ilike"> SQL Ödev 3 | </a>
 4. #### <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-4--distinct-ve-count">SQL Ödev 4 | </a>
 5. ####  <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-5--order-by--limit-ve-offset">SQL Ödev 5 | </a>
 6. ####  <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-6--aggregate-fonksiyonlar">SQL Ödev 6 | </a>
 7. #### <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-7--group-by--having">SQL Ödev 7 |</a>
 8. ####  <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-8--tablo-olu%C5%9Fturmak--verileri-g%C3%BCncellemek">SQL Ödev 8 | </a>
 9. ####  <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-9--inner-join">SQL Ödev 9 | </a>
 10. ####  <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-10--left-join-right-join-full-join">SQL Ödev 10 | </a>

 11. ####  <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-11--union-intersect-ve-except">SQL Ödev 11 |</a>

 12. ####  <a href="https://github.com/mucahidcanbey/sql_odevler_patika#sql-%C3%B6dev-12--sorgu-senaryolar%C4%B1">SQL Ödev 12 | </a>

<br>
<br>

<br>







## SQL Ödev 1 | WHERE ve Karşılaştırma & Mantıksal Operatörler

<br>
<br>
<br>

1-) <strong>film </strong>tablosunda bulunan <strong>title</strong> ve <strong>description</strong> 
sütunlarındaki verileri sıralayınız.



```

SELECT title, description FROM film;

```



<br>
<br>
<br>

2-) <strong>film</strong>  tablosunda bulunan tüm sütunlardaki verileri film uzunluğu <strong>(length)</strong>  60 dan büyük <strong>VE</strong>  75 ten küçük olma koşullarıyla sıralayınız.



```

SELECT * FROM film
WHERE length > 60 AND length < 75;

```



<br>
<br>
<br>

3-)  <strong>film</strong> tablosunda bulunan tüm sütunlardaki verileri  <strong>rental_rate</strong> 0.99  <strong>VE</strong>  <strong>replacement_cost</strong> 12.99  <strong>VEYA</strong> 28.99 olma koşullarıyla sıralayınız.



```

SELECT * FROM film
WHERE rental_rate = 0.99 AND replacement_cost = 12.99 
OR replacement_cost = 28.99;

```



<br>
<br>
<br>

4-) <strong>customer</strong> tablosunda bulunan <strong>first_name</strong> sütunundaki değeri 'Mary' olan müşterinin <strong>last_name</strong> sütunundaki değeri nedir?



```

SELECT last_name FROM customer
WHERE first_name = 'Mary';

```



<br>
<br>
<br>

5-) <strong>film</strong>  tablosundaki <strong>uzunluğu(length)</strong>  50 ten büyük OLMAYIP aynı zamanda <strong>rental_rate</strong>  değeri 2.99 <strong>veya</strong>  4.99 OLMAYAN verileri sıralayınız.

```

SELECT * FROM film
WHERE length <= 50 
AND NOT (rental_rate = 2.99 OR rental_rate = 4.99);

```

<br>
<br>
<br>

## SQL Ödev 2 | BETWEEN ve IN

<br>
<br>    
<br>

1-) <strong>film</strong> tablosunda bulunan tüm sütunlardaki verileri <strong>replacement cost</strong> değeri 12.99 dan büyük eşit ve 16.99 küçük olma koşuluyla sıralayınız ( BETWEEN - AND yapısını kullanınız.)

```

SELECT * FROM film 
WHERE replacement_cost BETWEEN 12.99 AND 16.99;

```



<br> 
<br>
<br>

2-) <strong>actor</strong> tablosunda bulunan <strong>first_name</strong> ve <strong>last_name</strong> sütunlardaki verileri <strong>first_name</strong> 'Penelope' veya 'Nick' veya 'Ed' değerleri olması koşuluyla sıralayınız. ( IN operatörünü kullanınız.)

```

SELECT first_name, last_name FROM actor 
WHERE first_name IN ('Penelope', 'Nick', 'Ed');

```


<br>
<br>
<br>

3-) <strong>film</strong> tablosunda bulunan tüm sütunlardaki verileri <strong>rental_rate</strong> 0.99, 2.99, 4.99 VE <strong>replacement_cost</strong> 12.99, 15.99, 28.99 olma koşullarıyla sıralayınız. ( IN operatörünü kullanınız.)

```

SELECT first_name, last_name FROM actor 
WHERE first_name IN ('Penelope', 'Nick', 'Ed');

```


<br>
<br>
<br>

## SQL Ödev 3 | LIKE ve ILIKE

<br>
<br>
<br>

1-)  <strong>country</strong> tablosunda bulunan  <strong>country</strong> sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.

```

SELECT country FROM country
WHERE country ~~ 'A%a' 

```



<br>
<br>
<br>

2-) <strong>country</strong> tablosunda bulunan <strong>country</strong> sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.

```

SELECT country FROM country 
WHERE country LIKE '_____%n' 

```


<br>
<br>
<br>

3-) <strong>film</strong> tablosunda bulunan <strong>title</strong> sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin <strong>'T'</strong> karakteri içeren film isimlerini sıralayınız.

```

SELECT title FROM film 
WHERE title ~~* '%T%T%T%T%' 

```


<br>
<br>
<br>

4-) <strong>film</strong> tablosunda bulunan tüm sütunlardaki verilerden <strong>title</strong> 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve <strong>rental_rate</strong> 2.99 olan verileri sıralayınız.

```

SELECT * FROM film 
WHERE title LIKE 'C%' AND length > 90 AND rental_rate = 2.99; 

```



<br>
<br>
<br>

## SQL Ödev 4 | DISTINCT ve COUNT

<br>
<br>
<br>

1-)  <strong>film</strong> tablosunda bulunan  <strong>replacement_cost</strong> sütununda bulunan birbirinden farklı değerleri sıralayınız.

```

SELECT DISTINCT replacement_cost FROM film

```


<br>
<br>
<br>

2-) <strong>film</strong> tablosunda bulunan <Strong>replacement_cost</strong> sütununda birbirinden farklı kaç tane veri vardır?

```

SELECT COUNT (DISTINCT replacement_cost) FROM film

```


<br>
<br>
<br>

3-) <strong>film</strong> tablosunda bulunan film isimlerinde  <strong>(title)</strong> kaç tanesini T karakteri ile başlar ve aynı zamanda  <strong>rating</strong> 'G' ye eşittir?

```

SELECT COUNT(*) FROM film 
WHERE title LIKE 'T%' AND rating = 'G';

```

<br>
<br>
<br>



4-) <strong>country</strong> tablosunda bulunan ülke isimlerinden (country) kaç tanesi <strong>5</strong> karakterden oluşmaktadır?


```

SELECT COUNT(DISTINCT country) FROM country 
where country like '_____';

```

<br>
<br>
<br>

5-) city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?

```

SELECT COUNT(city) FROM city 
WHERE city ILIKE 'R%'

```

<br>
<br>
<br>

## SQL Ödev 5 | ORDER BY | LIMIT ve OFFSET

<br>
<br>
<br>

1-) film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.

```

SELECT title, length
FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;

```



<br>
<br>
<br>

2-) film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.


```

SELECT title, length
FROM film
WHERE title LIKE '%n'
ORDER BY length ASC
LIMIT 5 OFFSET 5;

```



<br>
<br>
<br>

3-) customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.


```

SELECT *
FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;

```



<br>
<br>
<br>

## SQL Ödev 6 | Aggregate Fonksiyonlar

<br>
<br>
<br>

1-) film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?


```

SELECT ROUND(AVG(rental_rate),2) 
FROM film ;

```



<br>
<br>
<br>

2-) film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

```

SELECT COUNT(*)
FROM film
WHERE title LIKE 'C%';

```

<br>
<br>
<br>

3-) film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

```

SELECT MAX(length) 
FROM film 
WHERE rental_rate = 0.99;

```

<br>
<br>
<br>

4-) ffilm tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?


```

SELECT COUNT(DISTINCT replacement_cost) 
FROM film 
WHERE length > 150;

```

<br>
<br>
<br>

## SQL Ödev 7 | GROUP BY | HAVING

<br>
<br>
<br>

1-) film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.


```

SELECT rating, COUNT(*) FROM film
GROUP BY rating;

```


<br>
<br>
<br>

2-) film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.

```

SELECT replacement_cost, COUNT(*)
FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50

```

<br>
<br>
<br>

3-) customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?

```

SELECT store_id, COUNT(*) 
FROM customer
GROUP BY store_id;

```

<br>
<br>
<br>

 4-) city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.

 ```

SELECT country_id, COUNT(*) 
FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;

```

<br>
<br>
<br>

## SQL Ödev 8 | Tablo Oluşturmak | Verileri Güncellemek"

<br>
<br>
<br>

1-) test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.


```

CREATE TABLE employee (
  id INTEGER,
  name VARCHAR(50) NOT NULL,
  birthday DATE,
  email VARCHAR(100)
);

```


<br>
<br>
<br>

2-) Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.

```

insert into MOCK_DATA (id, name, birthday, email) values (1, 'Cobb', '1939/11/04', 'ckunert0@joomla.org');
insert into MOCK_DATA (id, name, birthday, email) values (2, 'Martina', '1953/09/19', null);
insert into MOCK_DATA (id, name, birthday, email) values (3, 'Alica', '1996/09/26', 'atilio2@wp.com');
insert into MOCK_DATA (id, name, birthday, email) values (4, 'Arnold', null, 'amarcroft3@dion.ne.jp');
insert into MOCK_DATA (id, name, birthday, email) values (5, 'Lanae', '1974/07/08', 'ldenziloe4@sourceforge.net');
insert into MOCK_DATA (id, name, birthday, email) values (6, 'Stephie', '1919/04/02', null);
insert into MOCK_DATA (id, name, birthday, email) values (7, 'Cordelie', '1982/03/26', null);
insert into MOCK_DATA (id, name, birthday, email) values (8, 'Shelby', '1931/07/29', null);
insert into MOCK_DATA (id, name, birthday, email) values (9, 'Celka', '1901/04/12', 'crulton8@fc2.com');
insert into MOCK_DATA (id, name, birthday, email) values (10, 'Mordecai', '1902/12/18', 'mlassen9@google.com');
insert into MOCK_DATA (id, name, birthday, email) values (11, 'Maria', '1930/10/22', 'mellesa@ucoz.com');
insert into MOCK_DATA (id, name, birthday, email) values (12, 'Ichabod', '1992/05/14', 'ievensdenb@1688.com');
insert into MOCK_DATA (id, name, birthday, email) values (13, 'Curran', null, null);
insert into MOCK_DATA (id, name, birthday, email) values (14, 'Yelena', '1926/09/28', 'yserckd@home.pl');
insert into MOCK_DATA (id, name, birthday, email) values (15, 'Yorke', '1915/07/09', 'yreaneye@lycos.com');
insert into MOCK_DATA (id, name, birthday, email) values (16, 'Allina', '1939/09/26', 'aburkwoodf@free.fr');
insert into MOCK_DATA (id, name, birthday, email) values (17, 'Jermaine', null, null);
insert into MOCK_DATA (id, name, birthday, email) values (18, 'Oliviero', '1903/11/20', 'oohickeyh@mapy.cz');
insert into MOCK_DATA (id, name, birthday, email) values (19, 'Emelyne', '1917/03/11', 'eferreirai@quantcast.com');
insert into MOCK_DATA (id, name, birthday, email) values (20, 'Julissa', '1985/09/22', null);
insert into MOCK_DATA (id, name, birthday, email) values (21, 'Myrna', '1944/03/27', 'mjagelsk@ihg.com');
insert into MOCK_DATA (id, name, birthday, email) values (22, 'Francisco', '1962/04/24', null);
insert into MOCK_DATA (id, name, birthday, email) values (23, 'Shep', '1933/12/27', 'scuttlerm@edublogs.org');
insert into MOCK_DATA (id, name, birthday, email) values (24, 'Ursulina', '1988/08/22', 'umallinsonn@hp.com');
insert into MOCK_DATA (id, name, birthday, email) values (25, 'Stearn', '1942/11/01', 'sdedricko@flickr.com');
insert into MOCK_DATA (id, name, birthday, email) values (26, 'Normy', '1981/08/26', 'nbrecherp@barnesandnoble.com');
insert into MOCK_DATA (id, name, birthday, email) values (27, 'Amalia', '1977/11/29', null);
insert into MOCK_DATA (id, name, birthday, email) values (28, 'Paulette', '1976/09/10', 'plotsr@stumbleupon.com');
insert into MOCK_DATA (id, name, birthday, email) values (29, 'Brietta', '1915/10/25', 'bcordss@t-online.de');
insert into MOCK_DATA (id, name, birthday, email) values (30, 'Cassandry', '1999/05/23', null);
insert into MOCK_DATA (id, name, birthday, email) values (31, 'Hercule', '1972/10/13', 'hmumu@hao123.com');
insert into MOCK_DATA (id, name, birthday, email) values (32, 'Bram', null, 'bbortolv@cisco.com');
insert into MOCK_DATA (id, name, birthday, email) values (33, 'Briano', '1923/01/08', null);
insert into MOCK_DATA (id, name, birthday, email) values (34, 'Peadar', '1951/03/15', 'pcordreyx@narod.ru');
insert into MOCK_DATA (id, name, birthday, email) values (35, 'Elfreda', '1990/11/10', 'ephilippsony@cam.ac.uk');
insert into MOCK_DATA (id, name, birthday, email) values (36, 'Tybalt', '1943/08/14', 'tkennetz@blinklist.com');
insert into MOCK_DATA (id, name, birthday, email) values (37, 'Jarib', '1910/10/22', 'jofer10@wordpress.org');
insert into MOCK_DATA (id, name, birthday, email) values (38, 'Godwin', '1953/12/27', 'gashbe11@nytimes.com');
insert into MOCK_DATA (id, name, birthday, email) values (39, 'Garvy', '1919/08/16', 'ggiffaut12@squidoo.com');
insert into MOCK_DATA (id, name, birthday, email) values (40, 'Shawn', '1984/07/07', null);
insert into MOCK_DATA (id, name, birthday, email) values (41, 'Gill', '1950/04/10', null);
insert into MOCK_DATA (id, name, birthday, email) values (42, 'Ambrosi', null, 'aludovico15@netscape.com');
insert into MOCK_DATA (id, name, birthday, email) values (43, 'Constantin', null, 'cbasilone16@clickbank.net');
insert into MOCK_DATA (id, name, birthday, email) values (44, 'Van', '1989/06/22', 'vdigwood17@odnoklassniki.ru');
insert into MOCK_DATA (id, name, birthday, email) values (45, 'Dugald', '1931/12/17', 'dlashbrook18@trellian.com');
insert into MOCK_DATA (id, name, birthday, email) values (46, 'Francklyn', '1930/02/05', null);
insert into MOCK_DATA (id, name, birthday, email) values (47, 'Ring', null, 'rthiolier1a@examiner.com');
insert into MOCK_DATA (id, name, birthday, email) values (48, 'Quentin', '1947/09/20', null);
insert into MOCK_DATA (id, name, birthday, email) values (49, 'Lurleen', '1978/06/01', 'lbegley1c@quantcast.com');
insert into MOCK_DATA (id, name, birthday, email) values (50, 'Clarke', '1925/10/18', null);

```

<br>
<br>
<br>

3-) Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.


```

// İsim (name) sütununu güncellemek:

UPDATE employee
SET name = 'John Doe'
WHERE name = 'Coob';


// Doğum günü (birthday) sütununu güncellemek:

UPDATE employee
SET birthday = '1990-06-15'
WHERE email = 'yserckd@home.pl';


// E-posta (email) sütununu güncellemek:

UPDATE employee
SET email = 'johndoe@example.com'
WHERE birthday = '1950/04/10';


// İsim ve doğum günü sütunlarını güncellemek:

UPDATE employee
SET name = 'Jane Smith',
    birthday = '1985-03-20'
WHERE id = 4;


// Tüm sütunları güncellemek:

UPDATE employee
SET name = 'Robert Johnson',
    birthday = '1978-12-10',
    email = 'robertjohnson@example.com'
WHERE id = 5;


```


<br>
<br>
<br>


4-) Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.



```

DELETE FROM employee
WHERE id = 44;

DELETE FROM employee
WHERE name ='Constantin';

DELETE FROM employee
WHERE name = 'Jane Smith' AND birthday = '1985-03-20';

DELETE FROM employee
WHERE email = 'umallinsonn@hp.com';

DELETE FROM employee
WHERE id >5
RETURNING *;

```


<br>
<br>
<br>

## SQL Ödev 9 | INNER JOIN

1-) city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.



```

SELECT city, country
FROM city
INNER JOIN country ON city.country_id = country.country_id;

```


<br>
<br>
<br>

2-) customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.


```

SELECT payment.payment_id, customer.first_name, customer.last_name
FROM customer
INNER JOIN payment ON customer.customer_id = payment.customer_id;

```


<br>
<br>
<br>

3-) customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.


```

SELECT rental.rental_id, customer.first_name, customer.last_name
FROM customer
INNER JOIN rental ON customer.customer_id = rental.customer_id;

```


<br>
<br>
<br>

## SQL Ödev 10 | LEFT JOIN, RIGHT JOIN, FULL JOIN

1-) city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.



```

SELECT city.city, country.country
FROM city
LEFT JOIN country ON city.country_id = country.country_id;

```


<br>
<br>
<br>

2-) customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.



```

SELECT payment.payment_id, customer.first_name, customer.last_name
FROM customer
RIGHT JOIN payment ON customer.customer_id = payment.customer_id;

```


<br>
<br>
<br>

3-) customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.



```

SELECT payment_id, first_name, last_name FROM payment
FULL JOIN customer ON customer.customer_id= payment.customer_id

```


<br>
<br>
<br>

## SQL Ödev 11 | UNION, INTERSECT ve EXCEPT

1-) actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.



```

SELECT first_name 
FROM actor
UNION 
SELECT first_name
FROM customer;

```


<br>
<br>
<br>

2-) actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.



```

SELECT first_name 
FROM actor
INTERSECT
SELECT first_name
FROM customer;

```


<br>
<br>
<br>

3-) actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.



```

SELECT first_name 
FROM actor 
EXCEPT 
SELECT first_name 
FROM customer;

```


<br>
<br>
<br>

4-) İlk 3 sorguyu tekrar eden veriler için de yapalım.



```

SELECT first_name 
FROM actor
UNION ALL
SELECT first_name
FROM customer;


SELECT first_name 
FROM actor
INTERSECT ALL
SELECT first_name
FROM customer;


SELECT first_name 
FROM actor 
EXCEPT ALL
SELECT first_name 
FROM customer;

```


<br>
<br>
<br>

## SQL Ödev 12 | Sorgu Senaryoları

1-) film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?



```

SELECT COUNT(*)
FROM film
WHERE length > (
  SELECT AVG(length)
  FROM film
);

```


<br>
<br>
<br>

2-) film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?


```

SELECT COUNT(*)
FROM film
WHERE rental_rate = (
  SELECT MAX(rental_rate)
  FROM film
);

```


<br>
<br>
<br>

3-) film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.


```

SELECT * FROM film
WHERE rental_rate = (
  SELECT MIN(rental_rate)
  FROM film
)
AND replacement_cost = (
  SELECT MIN(replacement_cost)
  FROM film
);

```


<br>
<br>
<br>

4-) payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.


```

SELECT customer_id, COUNT(*) AS transaction_count
FROM payment
GROUP BY customer_id
ORDER BY transaction_count DESC;


```



Bu repo'da [Patika](https://academy.patika.dev/) SQL eğitimindeki ödevler vardır. İçerisinde bir adet README dosyası barındırıyor.


## Installation

Öncelikle projeyi clonelayın.

```
https://github.com/mucahidcanbey/sql_odevler_patika.git
```

## Usage

Projeyi cloneladıktan sonra Visual Studio Code programında açınız.

Linux için:

```
cd sql_odevler_patika
code .
```

## Contributing
Pull requestler kabul edilir. Büyük değişiklikler için, lütfen önce neyi değiştirmek istediğinizi tartışmak için bir konu açınız.

## License
[MIT](https://choosealicense.com/licenses/mit/)

