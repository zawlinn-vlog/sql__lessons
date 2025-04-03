[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

## JOIN

Table နှစ်ခု သို့မဟုတ် နှစ်ခုထက်ပိုသော table record များကို စုပေါင်းထုတ်ချင်တဲ့အခါ JOIN ကို အသုံးပြုရပါတယ်။

အကြမ်းအားဖြင့် JOIN နှစ်မျိုးရှိပါတယ်

1. INNER JOIN
2. OUTER JOIN

### 1. INNER JOIN

INNER JOIN ဆိုတာ multiple table အတွင်းရှိ matching ဖြစ်နေသော value တွေကို ပေါင်းစည်ပီး ဆွဲထုတ်ပေးနိုင်ပါတယ်။

```sql
    SELECT column1, column2, column3...
    FROM table1
    INNER JOIN table2
    ON condition_1
    INNER JOIN table3
    ON condition_2
    ....
    ....
    INNER JOIN tableN
    ON condition_N;
```

```sql
    SELECT cus.name AS Customer_Name,
    cus.address AS Customer_Address,
    veh.name AS Vehicle_Brand,
    veh.price AS Vehicle_Value
    FROM customers AS cus
    INNER JOIN
    cars as veh
    ON
    cus.id = veh.cur_id
    ORDER BY
    Customer_Name;
```

### 2. OUTER JOIN

OUTER JOIN ကို multiple tables တွေ ချိတ်ဆက်အဖြေထုတ်မို့ အသုံးပြုပါတယ် သူကျ တစ်ဖက်က table မှာရှိတဲ့ Data အကုန်လုံးကို ဖော်ပြပေးပီး တဖက် table ကိုတော့ သူနဲ့ match ဖြစ်တဲ့အပိုင်းသာ ဖော်ပြပေးပီ match မဖိတဲ့ နေရာတွေကိုတော့ NULL တန်ဖိုးထည့်သွင်းပီးဖော်ပြပေးမာ ဖြစ်ပါတယ်။

- `Left (Outer) Join`: Retrieves all the records from the first table, Matching records from the second table and NULL values in the unmatched rows.
- `Right (Outer) Join`: Retrieves all the records from the second table, Matching records from the first table and NULL values in the unmatched rows.
- `Full (Outer) Join`: Retrieves records from both the tables and fills the unmatched values with `NULL`.

  <br/>

LEFT JOIN &mdash;

```sql
    SELECT cus.id, cus.name AS CUSTOMER_NAME,
    cus.address AS CUSTOMER_ADDRESS,
    veh.name AS VEHICLE_BRAND,
    veh.price AS VEHICLE_PRICE
    FROM customers AS cus
    LEFT JOIN
    cars AS veh
    ON
    cus.id = veh.cur_id
    ORDER BY
    cus.id;

```

<br/>
RIGHT JOIN &mdash;
<br/>

```sql
    SELECT cus.id AS CUSTOMER_ID,
    cus.name AS CUSTOMER_NAME,
    cus.address AS CUSTOMER_ADDRESS,
    veh.name AS VEHICLE_BRAND,
    veh.price AS VEHICLE_PRICE
    FROM customers AS cus
    RIGHT JOIN
    cars AS veh
    ON
    cus.id = veh.cur_id
    ORDER BY
    cus.id;
```

<br/>

FULL JOIN

<br/>

```sql
    SELECT cus.id AS CUSTOMER_ID,
    cus.name AS CUSTOMER_NAME,
    cus.address AS CUSTOMER_ADDRESS,
    veh.name AS VEHICLE_BRAND,
    veh.price AS VEHICLE_PIRCE
    FROM customers AS cus
    LEFT JOIN
    cars AS veh
    ON
    cus.id = veh.cur_id
    UNION
    SELECT cus.id AS CUSTOMER_ID,
    cus.name AS CUSTOMER_NAME,
    cus.address AS CUSTOMER_ADDRESS,
    veh.name AS VEHICLE_BRAND,
    veh.price AS VEHICLE_PIRCE
    FROM customers AS cus
    RIGHT JOIN
    cars AS veh
    ON
    cus.id = veh.cur_id;

```

> Let us summarize all the differences between the Left Join and Right Join in the table below −

| Left Join                                                                                                                                                                     | Right Join                                                                                                                                                                  |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Left Join matches the data of the first table or the left table with the data in second table. If the data is matched, the records are combined; otherwise, NULL is recorded. | Right Join matches the data of the second table or right table with the data in first table. If the data is matched, the records are combined; otherwise, NULL is recorded. |
| If the first table has less rows than the second table, extra unmatched rows from the second table are discarded.                                                             | If the second table has less rows than the first table, extra unmatched rows from the first table are discarded.                                                            |
| This Join is also known as Left Outer Join                                                                                                                                    | This Join is also known as Right Outer Join                                                                                                                                 |
| \*= is used in Transact SQL, instead of using the LEFT JOIN or LEFT OUTER JOIN query.                                                                                         | =\* is used in Transact SQL, instead of using the RIGHT JOIN or RIGHT OUTER JOIN query.                                                                                     |

                                                                                 |

### SELF JOIN

The SQL Self Join is used to join a table to itself as if the table were two tables. To carry this out, alias of the tables should be used at least once.

Self Join is a type of inner join, which is performed in cases where the comparison between two columns of a same table is required; probably to establish a relationship between them. In other words, a table is joined with itself when it contains both Foreign Key and Primary Key in it

```sql
    SELECT a.ID, b.NAME as EARNS_HIGHER, a.NAME
    as EARNS_LESS, a.SALARY as LOWER_SALARY
    FROM CUSTOMERS a, CUSTOMERS b
    WHERE a.SALARY < b.SALARY;
```

### CROSS JOIN

Table နှစ်ခုရဲ့ Data တွေကို mix လုပ်ပီထုတ်ချင်တဲ့အခါမှာ CROSS JOIN ကို အသုံးပြုရပါတယ်။

| id  | types |
| --- | ----- |
| 1   | A     |
| 2   | B     |
| 3   | C     |

<br>

| id  | style    |
| --- | -------- |
| 1   | Straight |
| 2   | Curly    |

```sql
    SELECT ht.types AS HairType,
    hs.style AS HairStyle
    FROM hairtypes AS ht
    CROSS JOIN
    hairstyles AS hs
    ORDER BY hs.style;
```

OUTPUT &mdash;

| HairType | HairStyle |
| -------- | --------- |
| A        | Curly     |
| C        | Curly     |
| B        | Curly     |
| C        | Straight  |
| B        | Straight  |
| A        | Straight  |

### DELETE JOIN

```sql
    DELETE a
    FROM CUSTOMERS AS a INNER JOIN ORDERS AS b
    ON a.ID = b.CUSTOMER_ID
    WHERE a.SALARY < 4500.00;
```

### UPDATE JOIN

```sql
    UPDATE table(s)
    JOIN table2 ON column3 = column4
    SET table1.column1 = value1, table1.column2 = value2, ...
    WHERE condition;
```

```sql
    UPDATE CUSTOMERS
    LEFT JOIN ORDERS
    ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID
    SET CUSTOMERS.SALARY = CUSTOMERS.SALARY + 1000
    WHERE ORDERS.CUSTOMER_ID = 3;
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
