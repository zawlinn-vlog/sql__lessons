[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

## MIN() and MAX();

The MIN() and MAX() functions in SQL are aggregate functions. They are used to compare values in a set and, retrieve the maximum and minimum values respectively.

> An aggregate function is a mathematical computation that takes a range of values as input and yields a single value expression, representing the significance of the provided data.

MAX() and MIN() aggregate functions are generally used in two ways:

- As functions, they are used with the GROUP BY clause of the SELECT statement.

- As expressions, they are used with a subquery and HAVING clause of SELECT statement.

```sql
    SELECT MAX(salary), MIX(salary)
    FROM customers;
```

```sql
    SELECT * FROM customers
    WHERE salary =  (SELECT MIN(salary)
    FROM customers);
```

### NULL in SQL &mdash;

SQL `NULL` functions are used to perform operations on `NULL` values that are stored in the database tables.

A `NULL` value serves as a placeholder in the database when data is absent or the required information is unavailable. It is a flexible value not associated to any specific data type and can be used in columns of various data types, including string, int, varchar, and more.

Following are the various features of a `NULL` value −

The `NULL` value is different from a zero value or a field containing a space. A record with a `NULL` value is one that has been left empty or unspecified during record creation.

The `NULL` value assists us in removing ambiguity from data. Thus, maintaining the uniform datatype across the column.

### SQL NULL Functions

To handle these `NULL` values in a database table, SQL provides various `NULL` functions. They are listed as follows −

- ISNULL()

- COALESCE()

- NULLIF()

- IFNULL()

### The ISNULL() Function

The SQL `ISNULL()` function returns 0 and 1 depending on whether the expression is null or not. If the expression is null, then this function returns 1; otherwise, it returns 0.

```sql
    SELECT salary,
    ISNULL(salary)
    FROM customers;
```

### The COALESCE() Function

The SQL `COALESCE()` function returns the first occurred NON-NULL expression among its arguments. If all the expressions are NULL, then the `COALESCE()` function will return NULL.

> An integer is evaluated first in the `COALESCE()` function, and an integer followed by a character expression always produces an integer as the output.

```sql
    SELECT NAME,
    SALARY,
    AGE,
    COALESCE(NULL, SALARY, AGE)
    AS Result FROM CUSTOMERS;
```

### The NULLIF() Function

The SQL `NULLIF()` function compares two expressions. If both expressions are the same, it returns NULL. Otherwise, it returns the first expression. This function can be used directly with clauses like SELECT, WHERE, and GROUP BY.

```sql
    SELECT NAME,
    ADDRESS,
    NULLIF(NAME, ADDRESS) AS Result
    FROM CUSTOMERS;
```

### The IFNULL() Function

The IFNULL() function replaces the NULL values in a database table with a specific value. This function accepts two arguments. If the first argument is a NULL value, it is replaced with the second argument. Otherwise, the first argument is returned as it is.

> This function does not work in the SQL Server database.

If both the arguments are NULL, the result of this function is also NULL.

```sql
    SELECT NAME,
    SALARY,
    IFNULL(SALARY, 5500) AS Result
    FROM CUSTOMERS;

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
