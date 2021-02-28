
# Devoir1

A1)
a)
![q1](https://user-images.githubusercontent.com/43187263/109407483-1e243a00-794f-11eb-9f9e-769d74617260.png)

b)
![q2](https://user-images.githubusercontent.com/43187263/109407542-a99dcb00-794f-11eb-975b-6902b15ba442.png)

c)
![q3](https://user-images.githubusercontent.com/43187263/109407555-bd493180-794f-11eb-8b21-a5748bba8f79.png)

A2)
![A2](https://user-images.githubusercontent.com/43187263/109407531-97239180-794f-11eb-9a5c-10245d8afed5.png)


A3)


B1)
a)
name   | experience
------------ | -------------
andrew | 3
august | 1
hayden | 2

b)
name   | software
------------ | -------------
MS Word | 2011-01-20
Sketch | 2016-06-15

c)Il faut enlever id du SELECT
```sql
WITH users_2019 (id, name) AS
 (SELECT *
 FROM users
 WHERE join_date BETWEEN '2019-01-01' AND '2019-12-31')
SELECT ~~id,~~
 name,
 count(licenses.access_code) AS num
FROM users_2019
LEFT JOIN licenses ON licenses.user_id = id
GROUP BY name
ORDER BY num DESC;
```
et on obtient:
name   | num
------------ | -------------
hayden | 1

B2)
a)
```sql
SELECT name,
join_date
FROM users
WHERE join_date < '2020-01-01';
```

b)

c)

d)
```sql
UPDATE softwares
SET version = '51', released_date = '2020-01-01'
WHERE name = 'Sketch';
```

B3)
d)
```sql
SELECT users, licenses
FROM users
INNER JOIN licenses
ON users.id = licenses.software_name;
```


















