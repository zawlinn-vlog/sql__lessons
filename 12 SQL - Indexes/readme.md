[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

## INDEXES

Table တွေထဲက data ကို မြန်မြန်ဆန်ဆန် ရယူနိုင်ရန် Index က လုပ်ဆောင်ပေးနိုင်ပါတယ်။ database ထဲမှာ ထည့်သွင်းထားသော data တွေကို pointer အနေဖြင့် အလုပ်လုပ်ပေးပီး database table ထဲက လိုအပ်တဲ့ data record တွေရဲ့ တည်နေရာကို လွယ်လွယ်ကူကူ ညွှန်ပြပေးမာ ဖြစ်ပါတယ်။

> SQL index တွေဟာ စာအုပ်တစ်အုပ်ရဲ့ မာတိကာ နာမည်တွေလို အလုပ်လုပ်ကြပါတယ်။

SQL indexes တွေဟာ database ထဲမှာ သိမ်းမို့ ကိုယ်ပိုင် storage space လိုအပ်ပါတယ်။ သူတို့ဟာ performance tools တွေဖိတဲ့အတွက် user က physically ကျိန်ုင်မှာမဟုတ်ပါဘူး

### INDEX အမျိုးအစားများ

1. Unique Index
2. Single-Column Index
3. Composite Index
4. Implicit Index

### 1. UNIQUE INDEX

unique index ကို perfomance အတွက်သာမက data integrity အတွက်ပါ အသုံးပြုပါသည်။ unique index တွေဟာ duplicate value တွေကို table ထဲ ထည့်သွင်းပေးမှာမဟုတ်ပါဘူး ခင်ဗျာ။ database table ကို applied လုပ်လိုက်အခါ user from ထဲကနေ duplicat value တွေ index table columns တွေမှာ ထည့်သွင်းမရအောင် PRIMARY and UNIQUE constraints တွေ auto ဖန်းတီးပေးမှာ ဖြစ်ပါတယ်။

#### CREATE INDEX

single column

```sql
    CREATE INDEX index_name ON tbname(colname);
```

multi-column

```sql
    CREATE INDEX index_name ON tbname(colname,colname,etc.);
```

#### DROP INDEX

```sql
    DROP INDEX index_name ON tbname;
```

performance အတွက် index ကို အသုံးပြုသောလည်း ရှောင်ရှားရမယ် အချက်လေးတွေရှိနေပါတယ်။

- INDEXES ကို small table တွေမှာ အသုံးမပြုသင့်ပါဘူး

- Table တွေမှာ အကြိမ်များစွာ အသုံးမပြုသင့်ပါဘူး၊ large batch update or insert operations.

- Index ကို NULL values တွေများစွာပါဝင်သော column မှာ အသုံးမပြုသင့်ပါဘူး

- ကြိမ်ဖန်များစွာ manipulate လုပ်တဲ့ column တွေဟာ index မဖြစ်သင့်ပါဘူး

> SQL index is a special lookup table that helps in efficiently searching or querying database tables of retrieve required data. for example, when we try to retrieve data from multiple tables using joins, indexes imporve the query performance.

### UNIQUE INDEX

SQL Unique index သည် rows နှစ်ခု table columns နှစ်ခုမှာ တူညီသော Data တွေ လက်ခံနိုင်ပေးပါတယ်။ သို့သော် Duplicate တွေ့တော့ ထည့်သွင်း၍ မရပါ ခင်ဗျာ။

- If the unique index is only created on a single column, the rows in that column will be unique.

- If a single column contains NULL in multiple rows, we cannot create a unique index on that column.

- If the unique index is created on multiple columns, the combination of rows in these columns will be unique.

- We cannot create a unique index on multiple columns if the combination of columns contains NULL in more than one row.

```sql
    CREATE UNIQUE INDEX unique_id ON tbname (colname)
```

```sql
    DROP INDEX unique_id ON tbname;
```

> Data in table is stored in the form of an unordered data structure called a "HEAP", where rows are placed without any specific order.Thus, when retrieving data from a table, the query optimizer must scan the entire table to located the requested rows. This process can be time-consuming, especially when we are dealing with large tables. To speed up the data retrieval, SQL provides a data object called index that stores and organized table data in a specific way, allowing faster data access.

### SQL Clustered Indexes

A clustered index in SQL is a type of index that determines the physical order in which the data values will be stored in a table.

When a clustered index is defined on a specific column, during the creation of a new table, the data is inserted into that column in a sorted order. This helps in faster retrieval of data since it is stored in a specific order.

- It is recommended to have only one clustered index on a table. If we create multiple clustered indexes on the same table, the table will have to store the same data in multiple orders which is not possible.

- When we try to create a primary key constraint on a table, a unique clustered index is automatically created on the table. However, the clustered index is not the same as a primary key. A primary key is a constraint that imposes uniqueness on a column or set of columns, while a clustered index determines the physical order of the data in the table.

> MySQL database does not have a separate provisions for Clustered and Non-Clustered indexes. Clustered indexes are automatically created when PRIMARY KEY is defined on a table. And when the PRIMARY KEY is not defined, the first UNIQUE NOT NULL key is treated as a Clustered index.

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
