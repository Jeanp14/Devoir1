# Devoir1


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

