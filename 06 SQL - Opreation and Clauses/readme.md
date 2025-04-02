[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

```sql
    CREATE TABLE CUSTOMERS (
    ID INT NOT NULL,
    NAME VARCHAR (20) NOT NULL,
    AGE INT NOT NULL,
    ADDRESS CHAR (25),
    SALARY DECIMAL (18, 2),
    PRIMARY KEY (ID)
    );
```

```sql
    INSERT INTO CUSTOMERS VALUES
    (1, 'Ramesh', 32, 'Ahmedabad', 2000.00 ),
    (2, 'Khilan', 25, 'Delhi', 1500.00 ),
    (3, 'Kaushik', 23, 'Kota', 2000.00 ),
    (4, 'Chaitali', 25, 'Mumbai', 6500.00 ),
    (5, 'Hardik', 27, 'Bhopal', 8500.00 ),
    (6, 'Komal', 22, 'Hyderabad', 4500.00 ),
    (7, 'Muffy', 24, 'Indore', 10000.00 );
```

#### `WHERE` Clauses ကို အသုံးပြုခြင်း

SQL မှာ WHERE ကို result ‌တွေ SELECT, UPDATE သို့မဟုတ် DELETE ပြုလုပ်ရန်အတွက် အသုံးပြုပါတယ်။ ဒါအပြင် multiple table တွေကို Join ပီး record တွေကိုလည်း ထုတ်ပေးနိုင်ပါတယ်။

```sql
    SELECT * FROM tbname WHERE [condition];
```

or

```sql
    SELECT col, col, etc. FROM tbname WHERE [condition];
```

> You can specify a condition using the comparison or logical operator such as, >, <, =, LIKE, NOT, etc.

#### `WHERE` Clause with `IN` Operator

ရှာလိုသော column ထဲ ရှာဖွေလိုသော value lists (val1, val2, val3 ...) ရှိသည့် record ကို ဆွဲထုတ်တဲ့အခါ `WHERE` -- `IN` Operator ကို အသုံးပြုပါတယ်။

> In some scenarios we may use multiple OR statements to include multiple conditions in SELECT, DELETE, UPDATE, or INSERT statements. Alternatively, we can use the IN operator instead of multiples OR statements.

```sql
    SELECT * FROM tbname
    WHERE col='val'
    OR col='val'
    OR col='val';
```

အဲလိုရေးမယ့်အစား

```sql
    SELECT col, col, etc. FROM tbname
    WHERE col
    IN ('val', 'val', 'val');
```

`IN` Operator ကို အသုံးပြု၍ ရပါတယ်။

```sql
    SELECT *|col... FROM tbname
    WHERE val IN (colname);
```

or

```sql
    SELECT *|col FROM tbname
    WHERE colname1
    IN (SELECT colname1 FROM tbname WHERE condition);
```

#### `WHERE` Clause with `NOT IN` Operator

ရှာလိုသော value ရှိသည့် record ကို ဖယ်၍ ကျန်သော record များကို ဆွဲထုတ်တဲ့အခါ WHERE -- NOT IN Operator ကို အသုံးပြုပါတယ်။

```sql
    SELECT col, col, etc. FROM tbname
    WHERE col
    NOT IN ('val', 'val', 'val');
```

#### `WHERE` Clause with `AND`, `OR`, `NOT` and `NOT EQUAL` Operator

တစ်ခုထက် ပိုသော condition တွေကို စစ်ထုတ်တဲ့အခါမှာ AND and OR ကို ခြားခံအနေဖြင့် ဆက်ပေးရပါတယ် ခင်ဗျာ။

```sql
    SELECT col, col, etc. FROM tbname
    WHERE (condition AND condition) OR condition;
```

```sql
    SELECT * FROM CUSTOMERS WHERE NOT (SALARY > 2000.00);
```

```sql
    SELECT * FROM CUSTOMERS WHERE name NOT IN (SALARY > 2000.00);
```

```sql
    SELECT name FROM CUSTOMERS WHERE name NOT LIKE 'k%';
```

```sql
    SELECT * FROM CUSTOMERS WHERE NOT NULL;
```

```sql
    SELECT * FROM CUSTOMERS
    WHERE SALARY NOT BETWEEN 1500.00 AND 2500.00;
```

```sql
    SELECT * FROM CUSTOMERS WHERE NOT EXISTS (
    SELECT CUR_ID FROM CARS
    WHERE CARS.CUR_ID = CUSTOMERS.ID);
```

```sql
    SELECT * FROM CUSTOMERS WHERE NOT SALARY != '2000';
```

```sql
    SELECT * FROM CUSTOMERS
    WHERE ADDRESS <> 'Bhopal' AND (SALARY > '2000' OR SALARY = '2000');
```

#### IS NULL OR IS NOT NULL

NULL vlaue ဆိုဘာ empty or unknown value ကိုခေါ်ဆိုတာ ဖြစ်ပါတယ်။ zero or empty string ကတော့ value တည်ရှိနေပီး null နှင့် မတူညီမပါ။ database record တွေဟာ null ဖြစ်လား မဖြစ်လား စစ်နိုင်တဲ့ operators နှစ်ခုရှိပါတယ်

- IS NULL
- IS NOT NULL

```sql
    SELECT COUNT(*) FROM orders WHER Qty IS NULL;
```

```sql
    SELECT COUNT(*) FROM orders WHER Qty IS NOT NULL;
```

> SQL (UPDATE, INSERT, DELETE) တို့နဲ့ တွဲဖက်၍ အသုံးပြုနိုင်ပါတယ် ခင်ဗျာ။

#### `BETWEEN` operator

Database ထဲက Record များထဲက integer, characters or dates တွေကို specified range အတွင်းဆွဲထုတ်ချင်တဲ့အခါ between operator ကို အသုံးပြုနိုင်ပါတယ်။

> You can use the BETWEEN operator to replace a combination of "greater than equal AND less than equal" conditions.

```sql
    SELECT column1, column2, column3,....columnN
    FROM table_name
    WHERE column BETWEEN value1 AND value2;
```

```sql
    SELECT * FROM CUSTOMERS
    WHERE SALARY BETWEEN 4000 AND 10000
    AND ADDRESS IN ('Hyderabad', 'Bhopal');
```

#### `DISTINCT` Keyword

ထပ်နေတဲ့ value တွေရှိတဲ့ column ကို distinct သုံးပီး စစ်ထုတ်တဲ့အခါ unique data ကိုသာ တွေ့ရမှာ ဖြစ်ပါတယ်။

```sql
    SELECT DISTINCT col, col, col, etc.
    FROM tbname |
    ORDER BY colname |
    WHERE [condition];
```

### `GROUP BY` Keyword

Database ထဲက record တွေကို ဆွဲထုတ်တဲ့အခါမှာ column တစ်ခုတည်းမှာ တည်ရှိသော တူညီသော data တွေကို စုစည်းပြီး ထုတ်ယူလို့ပါတယ် ခင်ဗျာ။ သူနဲ့ တွဲသုံးရတဲ့ function တွေရှိပါတယ်။ SUM(), COUNT(), AVG(), MAX(), MIN() and etc.

ဥပမာ - address တူနေတဲ့ record ဘနှခုရှိလဲ သိချင်တဲ့အခါမျိုး

```sql
    SELECT address, count(address)
    FROM dbname
    GROUP BY address;
```

> စုစည်းပီး ဆွဲထုတ်ထားတဲ့ record တွေကို filter လုပ်ချင်တဲ့အခါ HAVING ကို အသုံးပြုရပါတယ် WHERE clause သုံး၍ မရတော့ပါ။

```sql
    SELECT age, COUNT(name) FROM dbname
    GROUP BY age HAVING age > 24;
```

or

```sql
    SELECT age, COUNT(name) FROM dbname
    GROUP BY age HAVING age > 24 ORDER BY age ASC|DESC;
```

or

```sql
    SELECT age, COUNT(age) FROM dbname
    GROUP BY age HAVING COUNT(age) >= 2;
```

#### `LIKE` Operator

LIKE Operator သည် WILDCARD Operator နှင့်တွဲဖက် အသုံးပြုရပါတယ် ခင်ဗျာ။

Wildcard Operators

| Symbol | Description                                                   |
| ------ | ------------------------------------------------------------- |
| %      | Represents zero or more characters                            |
| \_     | Represents a single character                                 |
| []     | Represents any single character within the brackets \*        |
| ^      | Represents any character not in the brackets \*               |
| \-     | Represents any single character within the specified range \* |
| {}     | Represents any escaped character \*\*                         |

\* Not supported in PostgreSQL and MySQL databases. <br/>
\*\* Supported only in Oracle databases.

| S.No. | Wildcard & Description                                                                                         |
| ----- | -------------------------------------------------------------------------------------------------------------- |
| 1     | The percent sign (%)                                                                                           |
|       | Matches one or more characters.                                                                                |
|       | Note − MS Access uses the asterisk (\*) wildcard character instead of the percent sign (%) wildcard character. |
| 2     | The underscore (\_)                                                                                            |
|       | Matches one character.                                                                                         |
|       | Note − MS Access uses a question mark (?) instead of the underscore (\_) to match any one character.           |

star with word or character &mdash;

```sql
    SELECT colname FROM dbanme
    WHERE colname LIKE 'z%';
```

or

```sql
    SELECT colname FROM dbanme
    WHERE colname LIKE '_un';
```

| S.No. | Statement & Description                                                     |
| ----- | --------------------------------------------------------------------------- |
| 1     | WHERE SALARY LIKE '200%'                                                    |
|       | Finds any values that start with 200.                                       |
| 2     | WHERE SALARY LIKE '%200%'                                                   |
|       | Finds any values that have 200 in any position.                             |
| 3     | WHERE SALARY LIKE '\_00%'                                                   |
|       | Finds any values that have 00 in the second and third positions.            |
| 4     | WHERE SALARY LIKE '2*%*%'                                                   |
|       | Finds any values that start with 2 and are at least 3 characters in length. |
| 5     | WHERE SALARY LIKE '%2'                                                      |
|       | Finds any values that end with 2.                                           |
| 6     | WHERE SALARY LIKE '\_2%3'                                                   |
|       | Finds any values that have a 2 in the second position and end with a 3.     |
| 7     | WHERE SALARY LIKE '2\_\_\_3'                                                |
|       | Finds any values in a five-digit number that start with 2 and end with 3.   |

#### `ANY` | ALL Operators

The SQL `ANY` and ALL operators are used to perform a comparison between a single value and a range of values returned by the subquery.

eg.

```sql
    SELECT * FROM tbname
    WHERE colname > ANY
    (SELECT colname FROM tbname
    WHERE condition);
```

or

```sql
    SELECT colname FROM tbname
    GROUP BY colname
    HAVING colname
    > ANY (SELECT colname FROM tbname
    WHERE condition);
```

#### The SQL `EXISTS` Operator

The SQL `EXISTS` operator is used to verify whether a particular record exists in a MySQL table. While using this operator we need to specify the record (for which you have to check the existence) using a subquery.

The `EXISTS` operator is used in the WHERE clause of a SELECT statement to filter records based on the existence of related records in another table.

- It is a logical operator.

- It returns a Boolean value TRUE or FALSE.

- It returns TRUE if the subquery returns at least one record.

- If the EXISTS operator returns TRUE, the outer query will get executed; otherwise not.

- It can be used in SELECT, UPDATE, DELETE or INSERT statements.

```sql
    SELECT * from tbname
    WHERE EXISTS
    (SELECT foreign_id FROM tbname
    WHERE foreign_id=priamry_id AND condition);
```

<!-- `Checking for the existence of records in a many-to-many relationship` − The EXISTS operator can be used to check whether a record exists in a join table for a many-to-many relationship, for example, finding all customers who have purchased a particular product.

`Filtering records based on the existence of related records` − The EXISTS operator can be used to filter records based on the existence of related records in another table. For example, finding all orders that have associated order details.

`Aggregating data based on the existence of related records` − The EXISTS operator can be used to aggregate data based on the existence of related records. For example, finding the number of customers who have placed an order.

`Optimizing queries` − The EXISTS operator can be used to optimize queries by only returning the necessary data. For example, finding the first order for each customer without using a self-join. -->

#### mySQL CASE statement

SQL CASE statement သည် condition တစ်ခုချင်းစီးအတွက် သီးသန့် evaluate လုပ်နိုင်သလို သီးခြားဖော်ပြပေးနိုင်ပါတယ်။ `IF-THEN-ELSE` လို multiple conditions တွေကို စစ်ထုတ်၍ အလုပ်လုပ်ပုံနှင့် ဆင်တူပါတယ် ခင်ဗျာ။

```sql
    SELECT name, salary, CASE
    WHEN salary <= 4000 THEN "Lowest Paid"
    WHEN salary >= 10000 THEN "Hight Paid"
    ELSE "Normal Paid"
    END AS salary_status
    FROM customers;
```

and then

```sql
    SELECT
    CASE
        WHEN SALARY <= 4000 THEN 'Lowest paid'
        WHEN SALARY > 4000 AND SALARY <= 6500 THEN 'Average paid'
    ELSE 'Highest paid'
        END AS SALARY_STATUS,
    SUM(SALARY) AS Total
    FROM CUSTOMERS
    GROUP BY
    CASE
        WHEN SALARY <= 4000 THEN 'Lowest Price'
        WHEN SALARY > 4000 AND SALARY <= 6500 THEN 'Average Price'
    ELSE 'Highest Price'
    END;
```

```sql
    SELECT * FROM CUSTOMERS
    ORDER BY
    (CASE
        WHEN NAME LIKE 'k%' THEN NAME
        ELSE ADDRESS
    END);
```

```sql
    SELECT *, CASE
    WHEN SALARY < 4500 THEN (SALARY + SALARY * 25/100)
    ELSE SALARY
    END AS INCREMENT FROM CUSTOMERS;
```

#### UNION AND UNION ALL

- The tables to be combined must have the same number of columns with the same datatype.
- The number of rows need not be the same.

#### What is UNION? &mdash;

`UNION` is a type of operator/clause in SQL, that works similar to the union operator in relational algebra. It just combines the information from multiple tables that are union compatible.

> Only distinct rows from the tables are added to the resultant table, as UNION automatically eliminates all the duplicate records.

```sql
    SELECT * FROM table1
    UNION
    SELECT * FROM table2;
```

```sql
    SELECT * FROM table1
    UNION ALL
    SELECT * FROM table2;
```

#### The SQL INTERSECT Operator

The INTERSECT operator in SQL is used to retrieve the records that are identical/common between the result sets of two or more tables.

```sql
    SELECT colname|* FROM table1
    INTERSECT
    SELECT colname|* FROM table2;
```

#### The SQL EXCEPT Operator

The EXCEPT operator in SQL is used to retrieve all the unique records from the left operand (query), except the records that are present in the result set of the right operand (query).

```sql
    SELECT colname|* FROM table1
    EXCEPT
    SELECT colname|* FROM table2;
```

#### Aliases

You can rename a table or a column in a database temporarily by giving them another pseudo name. This pseudo name is known as Alias. The use of aliases is to address a specific table or a column in an SQL statement without changing their original name in the database. Aliases are created with the AS keyword.

```sql
    SELECT cus.fullname,
    cus.price,
    SUM(price) AS Total
    FROM clients AS cus;
```

<br>

<!-- ![Screenshot of Project](./s1.png) -->

What I use packages are &mdash;

[![My Skills](https://skillicons.dev/icons?i=mysql,npm,git,github,vscode&perline=3)](https://skillicons.dev)

<br>

[![PHP PREPROCESSOR: Introduction](https://img.shields.io/badge/PHP_PREPROCESSOR_—-000?style=for-the-badge—=ko-fi—=white)](#)

📫 Reach me out!

[![Facebook Badge](https://img.shields.io/badge/-@zawlinn_vlog-1ca0f1?style=flat&labelColor=1ca0f1&logo=facebook&logoColor=white&link=https://faebook.com/zawlinn_profile)](https://facebook.com/zawlinn.vlog)
[![youtube Badge](https://img.shields.io/badge/-zawlinn_vlog-c0392b?style=flat&labelColor=c0392b&logo=youtube&logoColor=white)](https://youtube.com/@zawlinn-vlog)
[![Gamil Badge](https://img.shields.io/badge/-zawlinn.profile-c0392b?style=flat&labelColor=c0392b&logo=gmail&logoColor=white)](mailto:zawlinn.profile@gmail.com)

<!-- TODO: Add last video link -->

<details>
    <summary>
        SQL - For short note
    </summary>
    <br/>

- :earth_asia: I’m currently working at @Mae Sot Market as a sale staff
- :computer: Most used line of code git commit -m "Initial Commit"
- :brain: I’m looking for help with Outstanding Video ideas.
- :mailbox_with_mail: How to reach me: zawlinn.profile@gmail.com.
- :heart: In a relationship with React
</details>
