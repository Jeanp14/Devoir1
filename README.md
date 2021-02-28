
# Devoir1

A1)
a)
![q1](https://user-images.githubusercontent.com/43187263/109407483-1e243a00-794f-11eb-9f9e-769d74617260.png)
b)![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)

c)![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)

A2)
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)

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

b)

c)

d)
```sql
UPDATE softwares
SET version = '51', released_date = '2020-01-01'
WHERE name = 'Sketch';
```





















