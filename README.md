# postgresql-practice
Задачи по майнору 3 курс

# Содержание
* [Задача 1](#1)
* [Задача 2](#2)
* [Задача 3](#3)
* [Задача 4](#4)
* [Задача 5](#5)
* [Задача 6](#6)
* [Задача 7](#7)
* [Задача 8](#8)
* [Задача 9](#9)
* [Задача 10](#10)
* [Задача 11](#11)
* [Задача 12](#12)
* [Задача 13](#13)
* [Задача 14](#14)
* [Задача 15](#15)
* [Задача 16](#16)
* [Задача 17](#17)
* [Задача 18](#18)
* [Задача 19](#19)
* [Задача 20](#20)
* [Задача 21](#21)
* [Задача 22](#22)
* [Задача 23](#23)
* [Задача 24](#24)
* [Задача 25](#25)
* [Задача 26](#26)
* [Задача 27](#27)
* [Задача 28](#28)
* [Задача 29](#29)
* [Задача 30](#30)
* [Задача 31](#31)
* [Задача 32](#32)
* [Задача 33](#33)
* [Задача 34](#34)
* [Задача 35](#35)
* [Задача 36](#36)
* [Задача 37](#37)
* [Задача 38](#38)
* [Задача 39](#39)
* [Задача 40](#40)
* [Задача 41](#41)
* [Задача 42](#42)
* [Задача 43](#43)
* [Задача 44](#44)
* [Задача 45](#45)
* [Задача 46](#46)
* [Задача 47](#47)
* [Задача 48](#48)
* [Задача 49](#49)
* [Задача 50](#50)
* [Задача 51](#51)
* [Задача 52](#52)
* [Задача 53](#53)
* [Задача 54](#54)
* [Задача 55](#55)
* [Задача 56](#56)
* [Задача 57](#57)
* [Задача 58](#58)
* [Задача 59](#59)
* [Задача 60](#60)
* [Задача 61](#61)
* [Задача 62](#62)
* [Задача 63](#63)
* [Задача 64](#64)
* [Задача 65](#65)
* [Задача 66](#66)
* [Задача 67](#67)
* [Задача 68](#68)
* [Задача 69](#69)
* [Задача 70](#70)
* [Задача 71](#71)
* [Задача 72](#72)
* [Задача 73](#73)
* [Задача 74](#74)
* [Задача 75](#75)
* [Задача 76](#76)
* [Задача 77](#77)
* [Задача 78](#78)
* [Задача 79](#79)
* [Задача 80](#80)
* [Задача 81](#81)
* [Задача 82](#82)
* [Задача 83](#83)
* [Задача 84](#84)
* [Задача 85](#85)
* [Задача 86](#86)
* [Задача 87](#87)
* [Задача 88](#88)
* [Задача 89](#89)
* [Задача 90](#90)
* [Задача 91](#91)
* [Задача 92](#92)
* [Задача 93](#93)
* [Задача 94](#94)
* [Задача 95](#95)
* [Задача 96](#96)
* [Задача 97](#97)
* [Задача 98](#98)
* [Задача 99](#99)
* [Задача 100](#100)


# Задачи

### 1
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=1">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT model, speed, hd
FROM PC
WHERE price < 500;
  </code></pre>
</details>

### 2
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=2">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT DISTINCT maker FROM Product WHERE type='Printer';
  </code></pre>
</details>

### 3
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=3">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT model, ram, screen from laptop where price > 1000;
  </code></pre>
</details>  
  
### 4
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=4">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT * from printer where color = 'y';
  </code></pre>
</details>   
  
### 5
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=5">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select model, speed, hd from pc where (cd = '12x' or cd = '24x') and price < 600;
  </code></pre>
</details> 
  
### 6
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=6">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select distinct p.maker as maker, l.speed as speed from laptop l join product p on l.model = p.model where l.hd >= 10;
  </code></pre>
</details>
  
### 7
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=7">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select distinct p.model, pc.price from product p join pc on p.model = pc.model where maker = 'B' union Select distinct p.model, l.price from product p join laptop l on p.model = l.model where maker = 'B' union Select distinct p.model, pr.price from product p join printer pr on p.model = pr.model where maker = 'B';
  </code></pre>
</details> 
  
### 8
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=8">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select maker from product where type = 'pc' except select maker from product where type = 'laptop';
  </code></pre>
</details>  
  
### 9
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=9">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select distinct p.maker from product p join pc pc on p.model = pc.model where pc.speed >= '450';
  </code></pre>
</details>  
  
### 10
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=10">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT DISTINCT model, price FROM printer where price = (SELECT MAX(price) FROM printer);
  </code></pre>
</details>    
  
### 11
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=11">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT AVG(speed) FROM PC;
  </code></pre>
</details>    
  
### 12
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=12">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select AVG(speed) from laptop where price > '1000';
  </code></pre>
</details>    
  
### 13
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=13">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select avg(pc.speed) from pc join product p on pc.model = p.model where maker = 'A';
  </code></pre>
</details>  
  
### 14
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=14">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select s.class, s.name, c.country from classes c join ships s on c.class = s.class where numguns >= '10';
  </code></pre>
</details>    
  
### 15
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=15">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT hd FROM PC group by hd having count(model) >= 2;
  </code></pre>
</details>    
  
### 16
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=16">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT DISTINCT A.model AS model, B.model AS model, A.speed As speed, A.ram As ram FROM PC AS A, PC B WHERE A.speed = B.speed AND A.ram = B.ram AND A.model > B.model;
  </code></pre>
</details>    
  
### 17
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=17">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT DISTINCT type, model, speed
FROM Laptop, (SELECT type FROM Product) AS Prod(type) WHERE speed < ALL (SELECT speed FROM PC) and type = 'laptop';
  </code></pre>
</details>    
  
### 18
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=18">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select distinct p.maker, pr.price from product p join printer pr on p.model = pr.model where pr.price = (SELECT MIN(price)
FROM printer where color = 'y') and pr.color = 'y';
  </code></pre>
</details>    
  
### 19
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=19">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select p.maker, AVG(l.screen) from product p join laptop l on p.model = l.model group by p.maker;
  </code></pre>
</details>    
  
### 20
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=20">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select maker, count(model) as Count_Model from product WHERE type = 'pc' group by maker having count(model) >= 3;
  </code></pre>
</details>      
  
### 21
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=21">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select p.maker, max(pc.price) as max_price from product p join pc pc on p.model = pc.model group by maker;
  </code></pre>
</details>      
  
### 22
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=22">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select speed, avg(price) from pc where speed > '600' group by speed;
  </code></pre>
</details>      
  
### 23
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=23">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select p.maker from product p join pc pc on p.model = pc.model where pc.speed >= '750' intersect Select p.maker from product p join laptop l on p.model = l.model where l.speed >= '750';
  </code></pre>
</details>      
  
### 24
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=24">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    WITH all_model AS (
SELECT model, price FROM pc
UNION ALL
SELECT model, price FROM printer
UNION ALL
SELECT model, price FROM laptop )
SELECT distinct model
FROM all_model WHERE price = ALL ( SELECT max(price) FROM all_model);
  </code></pre>
</details>      
  
### 25
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=25">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select distinct p.maker from product p join pc on p.model = pc.model where pc.ram = (select min(ram) from pc) and pc.speed = (SELECT MAX(speed) FROM pc WHERE ram = (SELECT MIN(ram) FROM pc)) and p.maker in (SELECT maker FROM product WHERE type = 'printer');
  </code></pre>
</details>   
  
### 26
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=26">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT AVG(price) as Avg_price FROM (SELECT price
FROM PC WHERE model IN (SELECT model FROM product WHERE maker='A' AND type='PC') UNION ALL SELECT price
FROM Laptop
WHERE model IN (SELECT model FROM product WHERE maker='A' AND
type='Laptop')
) AS prods;
  </code></pre>
</details>     
  
### 27
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=27">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT p.maker, avg(pc.hd) from product p join pc pc on p.model = pc.model WHERE pc.model IN (SELECT model FROM pc) AND maker IN (
SELECT maker FROM product WHERE type='printer') group by maker;
  </code></pre>
</details>    
  
### 28
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=28">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select count(maker) as qty from (SELECT distinct maker
FROM product group by maker having count(model) = 1) AS prod;
  </code></pre>
</details>    
  
### 29
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=29">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select i.point, i.date, inc, out from income_o i left join outcome_o o on i.point = o.point and i.date = o.date
union
Select o.point, o.date, inc, out from income_o i right join outcome_o o on i.point = o.point and i.date = o.date;
  </code></pre>
</details>    
  
### 30
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=30">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select point, date, SUM(sum_out), SUM(sum_inc)
from( select point, date, SUM(inc) as sum_inc, null as sum_out from Income Group by point, date
Union
select point, date, null as sum_inc, SUM(out) as sum_out from Outcome Group by point, date ) as t
group by point, date order by point;
  </code></pre>
</details>     
  
### 31
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=31">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select class, country from classes where bore >= '16';
  </code></pre>
</details>     
  
### 32
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=32">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select country, cast(avg((power(bore,3)/2)) as numeric(6,2)) as weight
from (select country, classes.class, bore, name from classes left join ships on classes.class=ships.class
union all
select distinct country, class, bore, ship from classes t1 left join outcomes t2 on t1.class=t2.ship
where ship=class and ship not in (select name from ships) ) a
where name!='null' group by country;
  </code></pre>
</details>     
  
### 33
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=33">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select ship from outcomes where result = 'sunk' and battle = 'North Atlantic';
  </code></pre>
</details>     
  
### 34
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=34">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select distinct name from classes, ships where launched >=1922 and displacement>35000 and type='bb' and
ships.class = classes.class;
  </code></pre>
</details>     
  
### 35
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=35">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select model, type from product where model NOT LIKE '%[^0-9]%' OR model NOT LIKE '%[^a-z]%';
  </code></pre>
</details>     
  
### 36
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=36">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select distinct c.class from classes c join outcomes o on c.class = o.ship
union
Select distinct c.class from classes c join ships s on c.class = s.class where s.class = s.name;
  </code></pre>
</details>     
  
### 37
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=37">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select class from(select class, name from ships
union
select class, ship as name from outcomes join classes on classes.class = outcomes.ship) as A
group by class having count(A.name)=1;
  </code></pre>
</details>     
 
### 38
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=38">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT country FROM classes where type = 'bb'
INTERSECT
SELECT country FROM classes where type = 'bc';
  </code></pre>
</details>   
  
### 39
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=39">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select distinct o.ship from outcomes o join battles b on o.battle = b.name where o.result = 'damaged' AND
EXISTS (SELECT battles.date
FROM battles join outcomes on outcomes.battle = battles.name
WHERE battles.date > b.date and outcomes.ship = o.ship);
  </code></pre>
</details>     
  
### 40
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=40">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select maker, type from product
where maker in (SELECT maker FROM
(SELECT maker, type FROM Product GROUP BY maker, type) Alias
group by maker having count(maker) = 1) group by maker, type having count(type)>1;
  </code></pre>
</details>     
  
### 41
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=41">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    with D as
(select model, price from PC
union
select model, price from Laptop
union
select model, price from Printer)

Select distinct P.maker,
CASE WHEN MAX(CASE WHEN D.price IS NULL THEN 1 ELSE 0 END) = 0 THEN
MAX(D.price) END
from Product P
right join D on P.model=D.model
group by P.maker;
  </code></pre>
</details>     
  
### 42
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=42">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select ship, battle from outcomes where result = 'sunk';
  </code></pre>
</details>     
  
### 43
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=43">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select name from battles where DATEPART(yy, date) not in (select DATEPART(yy, date)
from battles join ships on DATEPART(yy, date)=launched);
  </code></pre>
</details>     
  
### 44
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=44">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select name from ships where name like 'R%'
union
Select ship from outcomes where ship like 'R%';
  </code></pre>
</details>     
  
### 45
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=45">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select name from ships where name like '% % %'
union
Select ship from outcomes where ship like '% % %';
  </code></pre>
</details>     
  
### 46
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=46">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT DISTINCT ship, displacement, numguns
FROM classes LEFT JOIN ships ON classes.class=ships.class RIGHT JOIN outcomes ON classes.class=ship OR ships.name=ship
WHERE battle='Guadalcanal';
  </code></pre>
</details>     
  
### 47
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=47">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    WITH out AS (SELECT *
FROM outcomes JOIN (SELECT ships.name s_name, classes.class s_class, classes.country s_country
FROM ships FULL JOIN classes
ON ships.class = classes.class
) u
ON outcomes.ship=u.s_class
UNION
SELECT *
FROM outcomes JOIN (SELECT ships.name s_name, classes.class s_class, classes.country s_country
FROM ships FULL JOIN classes
ON ships.class = classes.class
) u
ON outcomes.ship=u.s_name)

SELECT fin.country
FROM (
SELECT DISTINCT t.country, COUNT(t.name) AS num_ships
FROM (
select distinct c.country, s.name
from classes c
inner join Ships s on s.class= c.class
union
select distinct c.country, o.ship
from classes c
inner join Outcomes o on o.ship= c.class) t
GROUP BY t.country

INTERSECT

SELECT out.s_country, COUNT(out.ship) AS num_ships
FROM out
WHERE out.result='sunk'
GROUP BY out.s_country) fin;
  </code></pre>
</details>     
  
### 48
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=48">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select class
from classes t1 left join outcomes t2 on t1.class=t2.ship where result='sunk'
union
select class
from ships left join outcomes on ships.name=outcomes.ship where result='sunk';
  </code></pre>
</details>     
  
### 49
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=49">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select s.name from ships s join classes c on s.name=c.class or s.class = c.class where c.bore = 16
union
select o.ship from outcomes o join classes c on o.ship=c.class where c.bore = 16;
  </code></pre>
</details>     
  
### 50
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=50">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select distinct o.battle from ships s join outcomes o on s.name = o.ship where s.class = 'kongo';
  </code></pre>
</details>     
  
### 51
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=51">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select NAME from(select name as NAME, displacement, numguns from ships inner join classes on ships.class = classes.class union select ship as NAME, displacement, numguns from outcomes inner join classes on outcomes.ship= classes.class) as d1 inner join (select displacement, max(numGuns) as numguns from ( select displacement, numguns from ships inner join classes on ships.class = classes.class union select displacement, numguns from outcomes inner join classes on outcomes.ship= classes.class) as f group by displacement) as d2 on d1.displacement=d2.displacement and d1.numguns =d2.numguns;
  </code></pre>
</details>     
  
### 52
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=52">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select s.name from ships s join classes c on s.class = c.class where country = 'japan' and (numGuns >= '9' or numGuns is null) and (bore < '19' or bore is null) and (displacement <= '65000' or displacement is null) and type='bb';
  </code></pre>
</details>     
  
### 53
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=53">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select CAST(AVG(numguns*1.0) AS NUMERIC(6,2)) as Avg_nmg from classes where type = 'bb';
  </code></pre>
</details>     
  
### 54
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=54">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select CAST(AVG(numguns*1.0) AS NUMERIC(6,2)) as AVG_nmg from (select ship, numguns, type from Outcomes join classes on ship = class
union
select name, numguns, type from ships s join classes c on c.class = s.class) as x where type = 'bb';
  </code></pre>
</details>     
  
### 55
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=55">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select c.class, min(s.launched) from classes c left join ships s on c.class = s.class group by c.class;
  </code></pre>
</details>     
  
### 56
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=56">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT c.class, COUNT(s.ship)
FROM classes c
LEFT JOIN (SELECT o.ship, sh.class
FROM outcomes o
LEFT JOIN ships sh ON sh.name = o.ship
WHERE o.result = 'sunk') AS s ON s.class = c.class OR s.ship = c.class
GROUP BY c.class;
  </code></pre>
</details>       
  
### 57
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=57">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT class, COUNT(ship) count_sunked
FROM (SELECT name, class FROM ships
      UNION
      SELECT ship, ship FROM outcomes) t
LEFT JOIN outcomes ON name = ship AND result = 'sunk'
GROUP BY class
HAVING COUNT(ship) > 0 AND COUNT(*) > 2;
  </code></pre>
</details>     
  
### 58
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=58">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT m, t,
CAST(100.0*cc/cc1 AS NUMERIC(5,2))
from
(SELECT m, t, sum(c) cc from
(SELECT distinct maker m, 'PC' t, 0 c from product
union all
SELECT distinct maker, 'Laptop', 0 from product
union all
SELECT distinct maker, 'Printer', 0 from product
union all
SELECT maker, type, count(*) from product
group by maker, type) as tt
group by m, t) tt1
JOIN (
SELECT maker, count(*) cc1 from product group by maker
) tt2
ON m=maker;
  </code></pre>
</details>     
  
### 59
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=59">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT c1, c2-
(CASE
WHEN o2 is null THEN 0
ELSE o2
END)
from
(SELECT point c1, sum(inc) c2 FROM income_o
group by point) as t1
left join
(SELECT point o1, sum(out) o2 FROM outcome_o
group by point) as t2
on c1=o1;
  </code></pre>
</details>       
  
### 60
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=60">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT c1, c2-
(CASE
WHEN o2 is null THEN 0
ELSE o2
END)
from
(SELECT point c1, sum(inc) c2 FROM income_o
where date<'2001-04-15'
group by point) as t1
left join
(SELECT point o1, sum(out) o2 FROM outcome_o
where date<'2001-04-15'
group by point) as t2
on c1=o1;
  </code></pre>
</details>       
  
### 61
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=61">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT sum(i) FROM
(SELECT point, sum(inc) as i FROM
income_o
group by point

UNION

SELECT point, -sum(out) as i FROM
outcome_o
group by point
) as t;
  </code></pre>
</details>     
  
### 62
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=62">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT
(SELECT sum(inc) FROM Income_o WHERE date<'2001-04-15')
-
(SELECT sum(out) FROM Outcome_o WHERE date<'2001-04-15')
AS remain;
  </code></pre>
</details>     
  
### 63
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=63">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT name FROM Passenger
WHERE ID_psg in
(SELECT ID_psg FROM Pass_in_trip
GROUP BY place, ID_psg
HAVING count(*)>1);
  </code></pre>
</details>       
  
### 64
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=64">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT i1.point, i1.date, 'inc', sum(inc) FROM Income,
(SELECT point, date FROM Income
EXCEPT
SELECT Income.point, Income.date FROM Income
JOIN Outcome ON (Income.point=Outcome.point) AND
(Income.date=Outcome.date)
) AS i1
WHERE i1.point=Income.point AND i1.date=Income.date
GROUP BY i1.point, i1.date
UNION
SELECT o1.point, o1.date, 'out', sum(out) FROM Outcome,
(SELECT point, date FROM Outcome
EXCEPT
SELECT Income.point, Income.date FROM Income
JOIN Outcome ON (Income.point=Outcome.point) AND
(Income.date=Outcome.date)
) AS o1
WHERE o1.point=Outcome.point AND o1.date=Outcome.date
GROUP BY o1.point, o1.date;
  </code></pre>
</details>     
  
### 65
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=65">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT row_number() over(ORDER BY maker,s),t, type FROM
(SELECT maker,type,
CASE
WHEN type='PC'
THEN 0
WHEN type='Laptop'
THEN 1
ELSE 2
END AS s,
CASE
WHEN type='Laptop' AND (maker in (SELECT maker FROM Product WHERE
type='PC'))
THEN 
WHEN type='Printer' AND ((maker in (SELECT maker FROM Product WHERE
type='PC')) OR (maker in (SELECT maker FROM Product WHERE
type='Laptop')))
THEN ''
ELSE maker
END AS t
FROM Product
GROUP BY maker,type) AS t1
ORDER BY maker, s;
  </code></pre>
</details>     
  
### 66
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=66">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT date, max(c) FROM
(SELECT date,count(*) AS c FROM Trip,
(SELECT trip_no,date FROM Pass_in_trip WHERE date>='2003-04-01' AND date<='2003-04-07' GROUP BY trip_no, date) AS t1
WHERE Trip.trip_no=t1.trip_no AND town_from='Rostov'
GROUP BY date
UNION ALL
SELECT '2003-04-01',0
UNION ALL
SELECT '2003-04-02',0
UNION ALL
SELECT '2003-04-03',0
UNION ALL
SELECT '2003-04-04',0
UNION ALL
SELECT '2003-04-05',0
UNION ALL
SELECT '2003-04-06',0
UNION ALL
SELECT '2003-04-07',0) AS t2
GROUP BY date;
  </code></pre>
</details>       
  
### 67
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=67">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select count(*) from
(SELECT TOP 1 WITH TIES count(*) c, town_from, town_to from trip
group by town_from, town_to
order by c desc) as t;
  </code></pre>
</details>     
  
### 68
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=68">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select count(*) from (
select TOP 1 WITH TIES sum(c) cc, c1, c2 from (
SELECT count(*) c, town_from c1, town_to c2 from trip
where town_from>=town_to
group by town_from, town_to
union all
SELECT count(*) c,town_to, town_from from trip
where town_to>town_from
group by town_from, town_to
) as t
group by c1,c2
order by cc desc
) as tt;
  </code></pre>
</details>     
  
### 69
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=69">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select
  row_number() over(order by maker) as num
  -- Выводим {maker} только если
  -- это первая строка
  ,CASE WHEN mnum=1 THEN maker
    ELSE ''
  END as maker
  ,type
  from (
    select
    -- Нумеруем {maker, type} для каждого {maker}
    row_number() over(partition by maker order by maker, ord) as mnum
    ,maker
    ,type
    from (
      -- Выбираем уникальные {maker, type},
      -- а также создаем доп. столбец {ord}
      -- для требуемой сортировки
    select
      distinct maker, type
      ,CASE WHEN LOWER(type)='pc' then 1
            WHEN LOWER(type)='laptop' then 2
            ELSE 3
      END as ord
      from product
    ) as mto
  ) as mtn;
  </code></pre>
</details>         
  
### 70
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=70">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT DISTINCT o.battle
FROM outcomes o
LEFT JOIN ships s ON s.name = o.ship
LEFT JOIN classes c ON o.ship = c.class OR s.class = c.class
WHERE c.country IS NOT NULL
GROUP BY c.country, o.battle
HAVING COUNT(o.ship) >= 3;
  </code></pre>
</details>          
  
### 71
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=71">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
  SELECT p.maker
FROM product p
LEFT JOIN pc ON pc.model = p.model
WHERE p.type = 'PC'
GROUP BY p.maker
HAVING COUNT(p.model) = COUNT(pc.model);
  </code></pre>
</details>     
  
### 72
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=72">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select TOP 1 WITH TIES name, c3 from passenger
join
(select c1, max(c3) c3 from
(
select pass_in_trip.ID_psg c1, Trip.ID_comp c2, count(*) c3 from pass_in_trip
join trip on trip.trip_no=pass_in_trip.trip_no
group by pass_in_trip.ID_psg, Trip.ID_comp
) as t
group by c1
having count(*)=1) as tt
on ID_psg=c1
order by c3 desc;
  </code></pre>
</details>     
  
### 73
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=73">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT DISTINCT c.country, b.name
FROM battles b, classes c
MINUS
SELECT c.country, o.battle
FROM outcomes o
LEFT JOIN ships s ON s.name = o.ship
LEFT JOIN classes c ON o.ship = c.class OR s.class = c.class
WHERE c.country IS NOT NULL
GROUP BY c.country, o.battle;
  </code></pre>
</details>       
  
### 74
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=74">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT c.country, c.class
FROM classes c
WHERE UPPER(c.country) = 'RUSSIA' AND EXISTS (
SELECT c.country, c.class
FROM classes c
WHERE UPPER(c.country) = 'RUSSIA' )
UNION ALL
SELECT c.country, c.class
FROM classes c
WHERE NOT EXISTS (SELECT c.country, c.class
FROM classes c
WHERE UPPER(c.country) = 'RUSSIA' );
  </code></pre>
</details>     
  
### 75
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=75">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select shipname,launched,batname
from
(select s.name as shipname,launched,b.name as batname,
row_number() over (partition by s.name order by "date") as num
from ships s,battles b
where to_char("date",'yyyy')>=launched
and launched is not null)
where num = 1
union
(
select name,launched,(select name from battles
where "date" = (select max("date") from battles)) as batname
from ships
where launched is null
);
  </code></pre>
</details>     
  
### 76
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=76">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    WITH cte AS
(SELECT ROW_NUMBER() OVER (PARTITION BY ps.ID_psg,pit.place ORDER BY pit.date) AS rowNumber
,DATEDIFF (minute, time_out, DATEADD(DAY,IIF(time_in<time_out,1,0),time_in)) AS timeFlight, ps.Id_psg, ps.name
FROM Pass_in_trip pit LEFT JOIN trip tr ON pit.trip_no = tr.trip_no
LEFT JOIN Passenger ps ON ps.ID_psg = pit.ID_psg -- Все рейсы
)
SELECT MAX(cte.name),SUM(timeFlight) FROM cte
GROUP BY cte.ID_psg
HAVING MAX(rowNumber) = 1;
  </code></pre>
</details>       
  
### 77
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=77">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT TOP 1 WITH TIES * FROM (
  SELECT COUNT (DISTINCT P.trip_no) count, date
  FROM Pass_in_trip P
  JOIN Trip T ON T.trip_no = P.trip_no AND town_from = 'Rostov'
  GROUP BY P.trip_no, date) X
ORDER BY 1 DESC;
  </code></pre>
</details>     
  
### 78
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=78">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT name, REPLACE(CONVERT(CHAR(12), DATEADD(m, DATEDIFF(m,0,date),0), 102),'.','-') AS first_day,
             REPLACE(CONVERT(CHAR(12), DATEADD(s,-1,DATEADD(m, DATEDIFF(m,0,date)+1,0)), 102),'.','-') AS last_day
FROM Battles;
  </code></pre>
</details>     
  
### 79
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=79">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT Passenger.name, A.minutes
FROM (SELECT P.ID_psg,
      SUM((DATEDIFF(minute, time_out, time_in) + 1440)%1440) AS minutes,
      MAX(SUM((DATEDIFF(minute, time_out, time_in) + 1440)%1440)) OVER() AS MaxMinutes
      FROM Pass_in_trip P JOIN
       Trip AS T ON P.trip_no = T.trip_no
      GROUP BY P.ID_psg
      ) AS A JOIN
 Passenger ON Passenger.ID_psg = A.ID_psg
WHERE A.minutes = A.MaxMinutes;
  </code></pre>
</details>           
  
### 80
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=80">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT DISTINCT maker
FROM product
WHERE maker NOT IN (
     SELECT maker
     FROM product
     WHERE type='PC' AND model NOT IN (
          SELECT model
          FROM PC));
  </code></pre>
</details>         
  
### 81
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=81">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT O.*
FROM outcome O
INNER JOIN
(
SELECT TOP 1 WITH TIES YEAR(date) AS Y, MONTH(date) AS M, SUM(out) AS ALL_TOTAL
FROM outcome
GROUP BY YEAR(date), MONTH(date)
ORDER BY ALL_TOTAL DESC
) R ON YEAR(O.date) = R.Y AND MONTH(O.date) = R.M;
  </code></pre>
</details>     
  
### 82
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=82">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    WITH CTE(code,price,number)
AS
(
SELECT PC.code,PC.price, number= ROW_NUMBER() OVER (ORDER BY PC.code)
FROM PC
)
SELECT CTE.code, AVG(C.price)
FROM CTE
JOIN CTE C ON (C.number-CTE.number)<6 AND (C.number-CTE.number)> =0
GROUP BY CTE.number,CTE.code
HAVING COUNT(CTE.number)=6;
  </code></pre>
</details>     
  
### 83
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=83">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT name
FROM Ships AS s JOIN Classes AS cl1 ON s.class = cl1.class
WHERE
CASE WHEN numGuns = 8 THEN 1 ELSE 0 END +
CASE WHEN bore = 15 THEN 1 ELSE 0 END +
CASE WHEN displacement = 32000 THEN 1 ELSE 0 END +
CASE WHEN type = 'bb' THEN 1 ELSE 0 END +
CASE WHEN launched = 1915 THEN 1 ELSE 0 END +
CASE WHEN s.class = 'Kongo' THEN 1 ELSE 0 END +
CASE WHEN country = 'USA' THEN 1 ELSE 0 END > = 4;
  </code></pre>
</details>         
  
### 84
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=84">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT C.name, A.N_1_10, A.N_11_21, A.N_21_30
FROM (SELECT T.ID_comp,
       SUM(CASE WHEN DAY(P.date) < 11 THEN 1 ELSE 0 END) AS N_1_10,
       SUM(CASE WHEN (DAY(P.date) > 10 AND DAY(P.date) < 21) THEN 1 ELSE 0 END) AS N_11_21,
       SUM(CASE WHEN DAY(P.date) > 20 THEN 1 ELSE 0 END) AS N_21_30
      FROM Trip AS T JOIN
       Pass_in_trip AS P ON T.trip_no = P.trip_no AND CONVERT(char(6), P.date, 112) = '200304'
      GROUP BY T.ID_comp
      ) AS A JOIN
 Company AS C ON A.ID_comp = C.ID_comp;
  </code></pre>
</details>     
  
### 85
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=85">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select maker
from product
group by maker
having count(distinct type) = 1 and
       (min(type) = 'pc' or
       (min(type) = 'printer' and count(model) > 2));
  </code></pre>
</details>     
  
### 86
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=86">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT maker,
       CASE count(distinct type) when 2 then MIN(type) + '/' + MAX(type)
                                 when 1 then MAX(type)
                                 when 3 then 'Laptop/PC/Printer' END
FROM Product
GROUP BY maker;
  </code></pre>
</details>       
  
### 87
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=87">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT DISTINCT name, COUNT(town_to) Qty
FROM Trip tr JOIN Pass_in_trip pit ON tr.trip_no = pit.trip_no JOIN
         Passenger psg ON pit.ID_psg = psg.ID_psg
WHERE town_to = 'Moscow' AND pit.ID_psg NOT IN(SELECT DISTINCT ID_psg
FROM Trip tr JOIN Pass_in_trip pit ON tr.trip_no = pit.trip_no
WHERE date+time_out = (SELECT MIN (date+time_out)
                       FROM Trip tr1 JOIN Pass_in_trip pit1 ON tr1.trip_no = pit1.trip_no
                       WHERE pit.ID_psg = pit1.ID_psg)
AND town_from = 'Moscow')
GROUP BY pit.ID_psg, name
HAVING COUNT(town_to) > 1;
  </code></pre>
</details>     
  
### 88
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=88">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT
 (SELECT name FROM Passenger WHERE ID_psg = B.ID_psg) AS name,
 B.trip_Qty,
 (SELECT name FROM Company WHERE ID_comp = B.ID_comp) AS Company
FROM (SELECT P.ID_psg, MIN(T.ID_comp) AS ID_comp, COUNT(*) AS trip_Qty, MAX(COUNT(*)) OVER() AS Max_Qty
      FROM Pass_in_trip AS P JOIN
       Trip AS T ON P.trip_no = T.trip_no
      GROUP BY P.ID_psg
      HAVING MIN(T.ID_comp) = MAX(T.ID_comp)
      ) AS B
WHERE B.trip_Qty = B.Max_Qty;
  </code></pre>
</details>     
  
### 89
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=89">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select Maker , count(distinct model) Qty from Product
group by maker
having count(distinct model) > = ALL
(select count(distinct model) from Product
group by maker)
or
count(distinct model) <= ALL
(select count(distinct model) from Product
group by maker);
  </code></pre>
</details>         
  
### 90
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=90">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select maker, model, type from
(
Select
row_number() over (order by model) p1,
row_number() over (order by model DESC) p2,
from Product
) t1
where p1 > 3 and p2 > 3;
  </code></pre>
</details>     
  
### 91
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=91">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select count(maker)
from product
where maker in
(
  Select maker from product
  group by maker
  having count(model) = 1
);
  </code></pre>
</details>     
  
### 92
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=92">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT Q_NAME
FROM utQ
WHERE Q_ID IN (SELECT DISTINCT B.B_Q_ID
                FROM (SELECT B_Q_ID
                        FROM utB
                        GROUP BY B_Q_ID
                        HAVING SUM(B_VOL) = 765) AS B
                WHERE B.B_Q_ID NOT IN (SELECT B_Q_ID
                                        FROM utB
                                        WHERE B_V_ID IN (SELECT B_V_ID
                                                          FROM utB
                                                          GROUP BY B_V_ID
                                                          HAVING SUM(B_VOL) < 255)));
  </code></pre>
</details>     
  
### 93
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=93">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select c.name, sum(vr.vr)
from
(select distinct t.id_comp, pt.trip_no, pt.date,t.time_out,t.time_in,--pt.id_psg,
case
     when DATEDIFF(mi, t.time_out,t.time_in)> 0 then DATEDIFF(mi, t.time_out,t.time_in)
     when DATEDIFF(mi, t.time_out,t.time_in)<=0 then DATEDIFF(mi, t.time_out,t.time_in+1)
end vr
from pass_in_trip pt left join trip t on pt.trip_no=t.trip_no
) vr left join company c on vr.id_comp=c.id_comp
group by c.name;
  </code></pre>
</details>         
        
### 94
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=94">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
   SELECT DATEADD(day, S.Num, D.date) AS Dt,
       (SELECT COUNT(DISTINCT P.trip_no)
        FROM Pass_in_trip P
               JOIN Trip T
                 ON P.trip_no = T.trip_no
                    AND T.town_from = 'Rostov'
                    AND P.date = DATEADD(day, S.Num, D.date)) AS Qty
FROM (SELECT (3 * ( x - 1 ) + y - 1) AS Num
        FROM (SELECT 1 AS x UNION ALL SELECT 2 UNION ALL SELECT 3) AS N1
               CROSS JOIN (SELECT 1 AS y UNION ALL SELECT 2 UNION ALL SELECT 3) AS N2
        WHERE (3 * ( x - 1 ) + y ) < 8) AS S,
       (SELECT MIN(A.date) AS date
        FROM (SELECT P.date,
                       COUNT(DISTINCT P.trip_no) AS Qty,
                       MAX(COUNT(DISTINCT P.trip_no)) OVER() AS M_Qty
                FROM Pass_in_trip AS P
                       JOIN Trip AS T
                         ON P.trip_no = T.trip_no
                            AND T.town_from = 'Rostov'
                GROUP BY P.date) AS A
        WHERE A.Qty = A.M_Qty) AS D;
  </code></pre>
</details>     
  
### 95
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=95">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    SELECT name,
    COUNT(DISTINCT CONVERT(CHAR(24),date)+CONVERT(CHAR(4),Trip.trip_no)),
    COUNT(DISTINCT plane),
    COUNT(DISTINCT ID_psg),
    COUNT(*)
FROM Company,Pass_in_trip,Trip
WHERE Company.ID_comp=Trip.ID_comp and Trip.trip_no=Pass_in_trip.trip_no
GROUP BY Company.ID_comp,name;
  </code></pre>
</details>     
  
### 96
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=96">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    with r as (select v.v_name,
       v.v_id,
       count(case when v_color = 'R' then 1 end) over(partition by v_id) cnt_r,
       count(case when v_color = 'B' then 1 end) over(partition by b_q_id) cnt_b
  from utV v join utB b on v.v_id = b.b_v_id)
select v_name
  from r
where cnt_r > 1
  and cnt_b > 0
group by v_name;
  </code></pre>
</details>       
    
### 97
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=97">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select code, speed, ram, price, screen
from laptop where exists (
  select 1 x
  from (
    select v, rank()over(order by v) rn
    from ( select cast(speed as float) sp, cast(ram as float) rm,
                  cast(price as float) pr, cast(screen as float) sc
    )l unpivot(v for c in (sp, rm, pr, sc))u
  )l pivot(max(v) for rn in ([1],[2],[3],[4]))p
  where [1]*2 <= [2] and [2]*2 <= [3] and [3]*2 <= [4]
);
  </code></pre>
</details>     
  
### 98
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=98">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    with CTE AS
(select
1 n, cast (0 as varchar(16)) bit_or,
code, speed, ram FROM PC
UNION ALL
select n*2,
cast (convert(bit,(speed|ram)&n) as varchar(1))+cast(bit_or as varchar(15))
, code, speed, ram
from CTE where n < 65536
)
select code, speed, ram from CTE
where n = 65536
and CHARINDEX('1111', bit_or )> 0;
  </code></pre>
</details>     
  
### 99
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=99">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    select point,
       "date" income_date,
       "date" + nvl(
                  min(case when diff > cnt then cnt else null end),
                  max(cnt)+1
                ) incass_date
from (select i.point,
             i."date",
             (trunc(o."date") - trunc(i."date")) diff, -- разница дней
             -- количество запрещенных для инкассации дней после прихода и до текущего запрещенного дня
             count(1) over (partition by i.point, i."date" order by o."date" rows between unbounded preceding and current row)-1 cnt
      from income_o i
               join (select point, "date", 1 disabled from outcome_o
                     union
                     select point, trunc("date"+7,'DAY'), 1 disabled from income_o) o
                 on i.point = o.point
      where o."date" > = i."date")
group by point, "date";
  </code></pre>  
  
### 100
Условие - <a href="https://sql-ex.ru/learn_exercises.php?LN=100">тык</a>
<details>
  <summary>
    Ответ
  </summary>
  <pre><code>
    Select distinct A.date , A.R, B.point, B.inc, C.point, C.out
From (Select distinct date, ROW_Number() OVER(PARTITION BY date ORDER BY code asc) as R From Income
Union Select distinct date, ROW_Number() OVER(PARTITION BY date ORDER BY code asc) From Outcome) A
LEFT Join (Select date, point, inc
                , ROW_Number() OVER(PARTITION BY date ORDER BY code asc) as RI FROM Income
           ) B on B.date=A.date and B.RI=A.R
LEFT Join (Select date, point, out
                , ROW_Number() OVER(PARTITION BY date ORDER BY code asc) as RO FROM Outcome
           ) C on C.date=A.date and C.RO=A.R;
  </code></pre>    
  
  
  
  
