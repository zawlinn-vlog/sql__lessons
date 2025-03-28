[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

## Table များ တည်ဆောက်ခြင်း &mdash; ?

Data တွေကို မတည့်သွင်းခင် တည်ဆောက်ထားသော Database များတွင် Table များကို တည်ဆောက်ထားရမည်

```sql
    CREATE TABLE IF NOT EXISTS tbname (colname datatype constriants, colname datatype constriants, colname datatype constriants,etc.);
```

### Table များကို နာမည်ပြောင်းခြင်း &mdash;

တည်ဆောက်ထားသော Table များကို တခါတရံ နာမည်ပြောင်းရန် လိုအပ်လာလိမ်မယ်။ ထို့အခါ

```sql
    ALTER TABLE oldtbname RENAME TO newtbname;
```

or

```sql
    RENAME TABLE oldtbname TO newtbname;
```

multi table တွေကို name ချိန်းချင်ရင်

```sql
    RENAME TABLE oldtbname1 TO newtbname1, oldtbname2 TO newtbname2;
```

## Table ကို TRUNCATE ပြုလုပ်ခြင်း

Table မှာရှိတဲ့ Data တွေကို တစ်ခါတည်း Default(စပီး table create လုပ်ခဲ့ပီးတဲ့အခြေအနေ) အတိုင်းပြန်ပြုလုပ်ချင်တဲ့အခါမှာ truncate ကို အသုံးပြုနိုင်ပါတယ်။

```sql
    TRUNCATE TABLE tbname
```

## တည်ဆောက်ထားသော Table ကို Clone ပြုလုပ်ချင်ရင် &mdash;

တခါတရံမှာ ကျတော်တို့ဟာ table အဟောင်းတွေကို ပြန်တည်ဆောက်ရတဲ့အခါမျိူးဖြစ်စေ backup လုပ်ချင်တဲ့အခါမျိုးဖြစ်စေ table ကို CLONE ပြုလုပ်နိုင်ပါတယ်။

CLONE သုံးမျိုးရှိပါတယ် &mdash;

1. Simple Cloning
2. Shallow Cloning
3. Deep Cloning

#### Simple Cloning in MySQL

Simple Clone ပြုလုပ်ခြင်းမှာ table အဟောင်းကအတိုင်း Column တွေနဲ့ အဲ့ column မှာ သတ်မှတ်ထားသော null and default value တွေကို original table အတိုင်း ဖန်တီးပီးတော့ record တွေကိုပါ Copied ယူပေးမှာ ဖြစ်ပါတယ်။ သို့ပေမဲ့ auto_increment နှင့် primary key တွေတော့ ပါမှာ မဟုတ်ပါဘူးခင်ဗျာ။

<!-- Simple cloning operation creates a new replica table from the existing table and copies all the records in newly created table. To break this process down, a new table is created using the CREATE TABLE statement; and the data from the existing table, as a result of SELECT statement, is copied into the new table.

Here, clone table inherits only the basic column definitions like the NULL settings and default values from the original table. It does not inherit the indices and AUTO_INCREMENT definitions.

Syntax
Following is the basic syntax to perform simple cloning in MySQL− -->

```sql
    CREATE TABLE IF NOT EXISTS newtable AS SELECT * FROM existingtable;
```

> Table ကို `CLONE` ပြုလုပ်သောအခါ `PRIMARY KEY` ပါလာမည်မဟုတ်ပါ။ `PRIMARY KEY` ပြုလည်သတ်မှတ်ပေးရန် လိုအပ်ပါတယ်။

#### Shallow Cloning in MySQL

Shallow Clone ပြုလုပ်ခြင်းမှာ table အဟောင်းကအတိုင်း Column တွေနဲ့ အဲ့ column မှာ သတ်မှတ်ထားသော attribute တွေကို original table အတိုင်း ဖန်တီးပီးတော့ record တွေတော့ Copied ယူပေးမှာ မဟုတ်ပါဘူး ခင်ဗျာ။ ဒါကြောင့် new table က empty table ဖြစ်နေမှာ ဖြစ်ပါတယ်။

<!-- Shallow cloning operation creates a new replica table from the existing table but does not copy any data records into newly created table, so only new but empty table is created.

Here, the clone table contains only the structure of the original table along with the column attributes including indices and AUTO_INCREMENT definition.. -->

```sql
    CREATE TABLE IF NOT EXISTS newtbname LIKE existing_tbname;
```

#### Deep Cloning in MySQL

Deep Clone ပြုလုပ်ခြင်းမှာ table အဟောင်းကအတိုင်း Column တွေနဲ့ အဲ့ column မှာ သတ်မှတ်ထားသော attribute တွေကို original table အတိုင်း ဖန်တီးပီးတော့ record တွေကိုပါ Copied ယူပေးမှာ ဖြစ်ပါတယ် ခင်ဗျာ။

<!-- Deep cloning operation is a combination of simple cloning and shallow cloning. It not only copies the structure of the existing table but also its data into the newly created table. Hence, the new table will have all the contents from existing table and all the attributes including indices and the AUTO_INCREMENT definitions.

Since it is a combination of shallow and simple cloning, this type of cloning will have two different queries to be executed: one with CREATE TABLE statement and one with INSERT INTO statement. The CREATE TABLE statement will create the new table by including all the attributes of existing table; and INSERT INTO statement will insert the data from existing table into new table. -->

```sql
    CREATE TABLE IF NOT EXISTS new_tbname LIKE existing_tbname;
    INSERT INTO new_tbname SELECT * FROM existing_tbname;
```

## Temporary Tables ဆိုတာ ဘာလဲ &mdash; ?

Temporary Data တွေကို သိမ်းဆည်းနိုင်ရန်အတွက် Temporary table တွေကိုလည်း တည်ဆောက်နိုင်ပါတယ်။ သူတို့ဟာ client session တည်ရှိအချိန်ထိသာ အလုပ်လုပ်နိုင်ပီး session destory ဖိသွားတာနက် တပြိုက်နက် auto delete ဖြစ်သွားနိုင်သလို manual လည်း ဖျက်ဆီးပစ်နိုင်ပါတယ် ခင်ဗျာ။ Permanent table တွေလို CRUD (Create, Insert, Update, Delete, JOIN, etc.) စသဖြင့် ပြုလုပ်နိုင်ပါတယ်

<!-- Temporary tables are pretty much what their name describes: they are the tables which are created in a database to store temporary data. We can perform SQL operations similar to the operations on permanent tables like CREATE, UPDATE, DELETE, INSERT, JOIN, etc. But these tables will be automatically deleted once the current client session is terminated. In addition to that, they can also be explicitly deleted if the users decide to drop them manually.

Various RDBMS, like MySQL, support temporary tables starting from version 3.23 onwards. If you are using an older version of MySQL than 3.23, you can't use temporary tables, but you can use heap tables.

As stated earlier, temporary tables will only last as long as the client session is alive. If you run the code in a PHP script, the temporary table will be destroyed automatically when the script finishes executing. If you are connected to the MySQL database server through a MySQL client program, then the temporary table will exist until you close the client connection or manually destroy the table. -->

```sql
    CREATE TEMPORARY TABLE table_name(
   column1 datatype,
   column2 datatype,
   column3 datatype,
   .....
   columnN datatype,
   PRIMARY KEY( one or more columns )
);
```

> temporary table တည်ဆောက်သောအခါ unique and primary key တွေကို နောက်ဆုံးမှာ Create လုပ်သင့်ပါတယ်။

#### တည်ဆောက်ထားသော Temporary Table များကို ဖျက်ချင်ရင် &mdash;

```sql
    DROP TEMPORARY TABLE tbname;
```

## တည်ဆောက်ထားသော Table များကို ဖျက်ချင်ရင် &mdash;

```sql
    DROP TABLE tbname;
```

or

```sh
    mysqladmin -u dbuser -p drop tbname;
```

## တည်ဆောက်ထားသော Table ထဲ Column တွေထပ်ထည့်မယ် &mdash;

တည်ဆောက်ထားသော table ထဲ column တွေ ရှိပီးသား Data တွေ မပျက်အောင် ထည့်မယ်ဆိုရင်

```sql
    ALTER TABLE tbname {ADD|DROP|MODIFY} COLUMN colname datatype constraint {first|after existingcolname};
```

or

```sql
    ALTER TABLE tbname {ADD|DROP|MODIFY} COLUMN colname datatype constraint {first|after existingcolname},
                       {ADD|DROP|MODIFY} COLUMN colname datatype constraint {first|after existingcolname},
                       {ADD|DROP|MODIFY} COLUMN colname datatype constraint {first|after existingcolname},
                                                etc.;
```

> `{ADD|DROP|MODITY}` အနောက် `COLUMN` က `Optional` ဖြစ်ပါတယ် ပါလည်းရသလို မပါလည်း ရပါတယ်။

> `first` ကို သုံးရင် column အားလုံးရဲ့ အရှေ့ဆုံးမှာ ထည့်သွားပေးမှာ ဖြစ်ပီးတော့ `after` ကို အသုံးပြုရင်တော့ `existingcolname` ရဲ့ အနောက်မှာ ထည့်သွင်းပေးသွားမာပဲ ဖြစ်ပါတယ်။

## Column ကို ပြန်ဖျက်ခြင်း &mdash;

ထည့်သွင်းထားသော col ကို ပြန်ဖျက်ချင်ရင်

```sql
    ALTER TABLE tbname DROP COLUMN colname;
```

## Column ကို နာမည်ပြန်ချိန်းခြင်း &mdash;

```sql
    ALTER TABLE tbname CHANGE COLUMN oldname newname datatype;
```

## သတ်မှတ်ထားသော Column ရဲ့ Data type ကို ချိန်းခြင်း

```sql
    ALTER TABLE tbname MODIFY COLUMN oldname newname datatype;
```

or

```sql
    ALTER TABLE tbname MODIFY COLUMN oldname newname datatype,
                       MODIFY COLUMN oldname newname datatype,
                       MODIFY COLUMN oldname newname datatype,
                       etc.;
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
