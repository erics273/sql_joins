## SQL JOINS

This cheatsheet is meant as a reference for SQL Joins.

#### JOIN (INNER JOIN) -- returns all records that exist in both left and right tables

![image03.png](https://tiy-learn-content.s3.amazonaws.com/7837d13c-image03.png)
```sql
SELECT t1.name, t2.grade	
	FROM student t1 INNER JOIN grades t2
	ON t1.student_id = t2.student_id;
```
#### LEFT JOIN (LEFT OUTER JOIN) -- returns ALL records in the left table and any matching records in the right table

![image01.png](https://tiy-learn-content.s3.amazonaws.com/e16b2284-image01.png)
```sql
SELECT t1.name, t2.grade	
	FROM student t1 LEFT JOIN grades t2
	ON t1.student_id = t2.student_id;
```
#### RIGHT JOIN (RIGHT OUTER JOIN) -- returns ALL records in right table and any matching records in the left table

![image05.png](https://tiy-learn-content.s3.amazonaws.com/f3ac2d6e-image05.png)
```sql
SELECT t1.name, t2.grade	
	FROM student t1 RIGHT JOIN grades t2
	ON t1.student_id = t2.student_id;
```
#### OUTER JOIN (FULL OUTER JOIN) -- return ALL records in BOTH tables and and joins records where left matches right

![image06.png](https://tiy-learn-content.s3.amazonaws.com/018405c6-image06.png)
```sql
SELECT t1.name, t2.grade	
	FROM student t1 OUTER JOIN grades t2
	ON t1.student_id = t2.student_id;
```
#### LEFT EXCLUDING JOIN -- returns records on the left that DO NOT have matches on the right
![image02.png](https://tiy-learn-content.s3.amazonaws.com/98093eec-image02.png)
```sql
SELECT t1.name, t2.grade	
	FROM student t1 LEFT JOIN grades t2
	ON t1.student_id = t2.student_id
	WHERE t2.student_id IS NULL;
```
#### RIGHT EXCLUDING JOIN -- returns records on the right table that DO NOT have matches on the left
![image00.png](https://tiy-learn-content.s3.amazonaws.com/6a897291-image00.png)
```sql
SELECT t1.name, t2.grade	
	FROM student t1 RIGHT JOIN grades t2
	ON t1.student_id = t2.student_id
	WHERE t1.student_id IS NULL;
```
#### OUTER EXCLUDING JOIN -- returns ALL records from left and right where where records DO NOT match
![image04.png](https://tiy-learn-content.s3.amazonaws.com/e1a915b6-image04.png)
```sql
SELECT t1.name, t2.grade	
	FROM student t1 OUTER JOIN grades t2
	ON t1.student_id = t2.student_id
	WHERE t1.student_id IS NULL
	OR t2.student_id IS NULL;
```
