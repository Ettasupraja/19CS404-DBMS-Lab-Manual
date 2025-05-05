**Question 1**
--
![WhatsApp Image 2025-05-05 at 10 26 52_cd3895a3](https://github.com/user-attachments/assets/b0f993f3-5ca3-4632-af0e-6c2350813844)

```sql
SELECT id, name, age, city, income
FROM Employee
WHERE age < (
    SELECT AVG(age)
    FROM Employee
    WHERE income > 1000000
);

```

**Output:**

![WhatsApp Image 2025-05-05 at 10 28 24_21f55890](https://github.com/user-attachments/assets/3edd1547-e705-4bc9-aae0-2bd98520c08a)


**Question 2**
---
![WhatsApp Image 2025-05-05 at 10 29 02_1c97fb31](https://github.com/user-attachments/assets/907ef6a3-66b1-4530-85c8-bdf12dc91356)


```sql
SELECT department_id, department_name
FROM Departments
WHERE LENGTH(department_name) > (
    SELECT AVG(LENGTH(department_name))
    FROM Departments
);


```

**Output:**

![WhatsApp Image 2025-05-05 at 10 29 47_9e505aff](https://github.com/user-attachments/assets/76c97f9e-3a4b-42fa-83dd-225453d28ecc)


**Question 3**
---
![WhatsApp Image 2025-05-05 at 10 30 26_cd8b14b4](https://github.com/user-attachments/assets/0e90fa56-c9e5-477e-a748-1b042e8b4dad)


```sql
SELECT commission 
FROM salesman 
WHERE salesman_id IN 
(SELECT salesman_id 
FROM customer
WHERE city = 'Paris');
```

**Output:**

![WhatsApp Image 2025-05-05 at 11 01 15_3b3e3f72](https://github.com/user-attachments/assets/66927de3-e73f-46e7-a073-1eddd5ea5a27)


**Question 4**
---
![WhatsApp Image 2025-05-05 at 10 34 36_8da5bf63](https://github.com/user-attachments/assets/7b56a184-53d6-4543-837b-09845671ec0b)


```sql
SELECT *
FROM CUSTOMERS
WHERE ADDRESS = 'Delhi';

```

**Output:**

![WhatsApp Image 2025-05-05 at 10 35 25_8a9ecb53](https://github.com/user-attachments/assets/a2636100-70a5-4cdb-ae07-c5fec7e43007)

**Question 5**
---
![WhatsApp Image 2025-05-05 at 10 36 04_0232502f](https://github.com/user-attachments/assets/0704f3bd-322e-404d-a94a-01a84f13792c)

```sql
SELECT *
FROM CUSTOMERS
WHERE SALARY > 1500;

```

**Output:**

![WhatsApp Image 2025-05-05 at 10 36 58_b6d1c87e](https://github.com/user-attachments/assets/86fabafe-4442-4978-845b-fdbe63e06d30)


**Question 6**
---

![WhatsApp Image 2025-05-05 at 10 37 33_4d337f19](https://github.com/user-attachments/assets/96fb9714-6548-475e-993e-0cd08b72d333)

```sql
SELECT o.ord_no, o.purch_amt, o.ord_date, o.customer_id, o.salesman_id
FROM ORDERS o
JOIN SALESMAN s ON o.salesman_id = s.salesman_id
WHERE s.city = 'New York';

```

**Output:**

![WhatsApp Image 2025-05-05 at 10 38 40_c1462b14](https://github.com/user-attachments/assets/0ce3008e-ec15-412b-9e37-9d2feb7f0b21)


**Question 7**
---
![WhatsApp Image 2025-05-05 at 10 58 01_abed6229](https://github.com/user-attachments/assets/fd2f030b-6bf3-4295-8299-13c3bd9478b2)

```sql
SELECT ord_no, purch_amt, ord_date, customer_id, salesman_id
FROM orders
WHERE salesman_id IN (
    SELECT DISTINCT salesman_id
    FROM orders
    WHERE customer_id = 3007
);

```

**Output:**

![WhatsApp Image 2025-05-05 at 11 02 54_287a6307](https://github.com/user-attachments/assets/b513f463-531c-4c71-8306-0215d596b38f)


**Question 8**
---
![WhatsApp Image 2025-05-05 at 10 41 10_d0a317a6](https://github.com/user-attachments/assets/00575396-64f1-4ede-94c7-e5ca109e2ff3)


```sql
SELECT student_id, student_name, subject, grade
FROM Grades g
WHERE grade = (
    SELECT MAX(grade)
    FROM Grades
    WHERE subject = g.subject
)

```

**Output:**

![WhatsApp Image 2025-05-05 at 10 42 56_263174ed](https://github.com/user-attachments/assets/ab4b514c-660b-4c79-8d71-4629914c0933)


**Question 9**
---
![WhatsApp Image 2025-05-05 at 10 43 29_05c71b5d](https://github.com/user-attachments/assets/ba0eb468-97ed-451b-938e-5e479c7d8005)

```sql
SELECT *
FROM CUSTOMERS
WHERE SALARY = 1500;

```

**Output:**

![WhatsApp Image 2025-05-05 at 10 44 19_c0d79cee](https://github.com/user-attachments/assets/a0120957-ea02-476c-8bea-314e8d5d57ac)


**Question 10**
---
![WhatsApp Image 2025-05-05 at 10 56 40_ada0f822](https://github.com/user-attachments/assets/32699743-f659-4619-a22b-ee1e7e568127)


```sql
SELECT student_id, student_name, subject, grade
FROM Grades g
WHERE grade = (
    SELECT MIN(grade)
    FROM Grades
    WHERE subject = g.subject
)

```

**Output:**

![WhatsApp Image 2025-05-05 at 10 57 25_f7cd52b6](https://github.com/user-attachments/assets/a2d0f8c4-de63-425a-92d8-039ffcbd37f7)

**RESULT**
Thus, the SQL queries to implement subqueries and views have been executed successfully.
