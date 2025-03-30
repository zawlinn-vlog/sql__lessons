[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

## Database ထဲ data တွေကို ထည့်သွင်းခြင်း &mdash; ?

Database ထဲ Data တွေ ထည့်သွင်းတော့မယ်ဆိုရင်

1. `INSERT INTO` tbname ...
2. `INSERT INTO` .... `SELECT`

#### 1. INSERT INTO tbname

User ဆီက Information တွေကို သိမ်းမယ်ဆိုရင် ဒီ Method ကို အသုံးပြုရပါတယ်။

```sql
    INSERT INTO tbname (col, col, col, etc.)
    VALUE ('value', 'value', 'value', etc.);
```

or

```sql
    INSERT INTO tbname (col, col, col, etc.)
    VALUES ('value', 'value', 'value', etc.);
```

Data တွေ back up လုပ်လိုသော အခါနှင့် Clone လုပ်လိုသော အခါတွေမှာတော့

```sql
    INSERT INTO clone_tbname
    SELECT * FROM original_tbname;
```

or

```sql
    INSERT INTO clone_tbname (col,col,col,etc.)
    SELECT (col,col,col,etc.) FROM original_tbname;
```

### Database ထဲမှာ Data များ ဆွဲထုတ်ခြင်း

Database ထဲမှ Data များကို ဆွဲထုတ်တော့မယ်ဆိုရင်တော့ `SELECT` keyword ကို အသုံးပြုပါတယ်။

```sql
    SELECT * FROM tbname;
```

or

```sql
    SELECT col, col, etc. FROM tbname;
```

or

```sql
    SELECT * FROM tbname
    WHERE {condition|expression};
```

or

```sql
    SELECT col, col, etc. FROM tbname
    WHERE {condition|expression};
```

### Database ထဲမှ Data များကို Update ပြုလုပ်ခြင်း &mdash;

SQL `UPDATE` Statement သည် Database ထဲက record များကို ပြင်ဆင်ပေးပါသည်။ DML - Data Manipulation Language ရဲ့ အစိတ်အပိုင်းတစ်ခုဖြစ်ပြီးတော့ table ရဲ့ကို ထိခိုက်ခြင်းမရှိဘဲ Record များကို ပြင်ဆင်ပေးနိုင်ပါတယ်။

> `UPDATE` လုပ်တဲ့အခါ Filter(WHERE clause) ပါဝင်ရန်လိုအပ်ပါတယ်။ filter မပါက record အားလုံးပေါ် သက်ရောက်သွားမှာ ဖြစ်ပါတယ်။

<!-- To filter records that needs to be modified, you can use a WHERE clause with UPDATE statement. Using a WHERE clause, you can either update a single row or multiple rows. -->

```sql
    UPDATE tbname SET col="data"
    WHERE {condition|expression};
```

or

```sql
    UPDATE tbname SET col='data', col='data'
    WHERE {condition|expression};
```

### Database ထဲမှာ Data များကို Delete ပြုလုပ်ခြင်း &mdash;

SQL `DELETE` Statement သည် Database ထဲက record များကို DELETE ပြုလုပ်ပေးပါသည်။

```sql
    DELETE FROM tbname WHERE [condition];
```

> If you execute `DELETE` statement without a WHERE clause, it will delete all the records from the table.

### Record များကို Sorting ပြုလုပ်ခြင်း

Database record များကို ဆွဲထုတ်တဲ့အခါမှာ sorting စီပီး ထုတ်လို့ပါတယ်။ ဒါမှမဟုတ်ရင် record များက First come first serve အနေနဲ့အလုပ်လုပ်သွားမှာ ဖြစ်ပါတယ်။

```sql
    SELECT * FROM tbname
    ORDER BY col,col,col [ASC|DESC];
```

or

```sql
    SELECT * FROM CUSTOMERS ORDER BY (
        CASE ADDRESS
        WHEN 'MUMBAI' THEN 1
        WHEN 'DELHI' THEN 2
        WHEN 'HYDERABAD' THEN 3
        WHEN 'AHMEDABAD' THEN 4
        WHEN 'INDORE' THEN 5
        WHEN 'BHOPAL' THEN 6
        WHEN 'KOTA' THEN 7
        ELSE 100 END
        );
```

<!-- The SQL ORDER BY clause is used to sort the data in ascending or descending order, based on one or more columns. By default, some databases sort the query results in an ascending order.

In addition to that, ORDER BY clause can also sort the data in a database table in a preferred order. This case may not sort the records of a table in any standard order (like alphabetical or lexicographical), but, they could be sorted based on any external condition. For instance, in an ORDERS table containing the list of orders made by various customers of an organization, the details of orders placed can be sorted based on the dates on which those orders are made. This need not be alphabetically sorted, instead, it is based on "first come first serve". -->

### Virtual View Database ကို ဖန်တီးခြင်း

A view in SQL is a virtual table that is sotred in the database with an associated name. It is a composition of a table in the form of a predefined SQL query. A view can contain rows from an existing table (All or SELECTED). A view can be created from one or many tables. Unless indexed, a view does not exist a database.

The data in the view does not exist in the database physically. A view is typically created by the database administrator and is used to &mdash;

- Structure data in a way that user or classes of users find natural intuitive.
- Restrict access to the data in such a way that a user can see and (somtimes) modify exactly what they need and no more
- Summarize data from various tables which can be used to generate reports.

```sql
    CREATE VIEW veiw_tbname AS
    SELECT * FROM existing_tbname;
```

or

```sql
    CREATE VIEW veiw_tbname AS
    SELECT col, col, col, etc...
    FROM existing_tbname WHERE [condition];
```

or

```sql
    CREATE VIEW veiw_tbname AS
    SELECT col, col, col, etc...
    FROM existing_tbname
    WHERE [condition] WITH CHECK OPTION;
```

### Update View table

view table က record တွေကို `UPDATE` လုပ်တဲ့အခါ original table က record တွေက လိုက်ပီး ပြောင်းသွားပါတယ်။

```sql
    UPDATE view_tbname
    SET col='value', col='value', col='value', etc...
    WHERE [condition]
```

### View Table ကို နာမည်ပြောင်းခြင်း

```sql
    RENAME TABLE old_view_tbname TO new_view_tbname;
```

### View Table ကို ပြန်ဖျက်ခြင်း

```sql
    DROP VIEW veiw_tbname;
```

or

```sql
    DROP VIEW IF EXISTS veiw_tbname;
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
