[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

## Primary ဆိုတာ ဘာလဲ &mdash; ?

The SQL Primary Key
The SQL Primary Key is a column (or combination of columns) that uniquely identifies each record in a database table. The Primary Key also speeds up data access and is used to establish a relationship between tables.

> Even though a table can only have one Primary Key, it can be defined on one or more fields. When a primary key is created on multiple fields of a table, it is called a Composite Key.

Let us say, you are developing an application called "Customer Management System" to handle all the customer data of a member-only resort. This data can include their personal details, assigned member IDs, other details of the membership they opted, etc. And in all the tables created within this database, the member ID is used to distinguish the customers from each other. So, this field will be the Primary Key.

Following is the diagram of a CUSTOMERS table that holds the personal details of the customers. And as we can observe, the primary key is defined on the CUST_ID column. Using this primary key, we can retrieve a unique record of any customer.

Primary key ဆိုတာ table တစ်ခုမှ unique ဖိတဲ့ indentifier တစ်ခုဖြစ်တဲ့ပါတယ်။ unique values တွေ ပါနိုင်ပီး NULL ဖြစ်လို့တော့ မရပါဘူး ခင်ဗျာ။ နောက်ပီးတော့ table တစ်ခုမှာ primary key တစ်ခုသာ ရှိရပါမယ်။ သို့သော် အဲ primary key တစ်ခုမှာ column က တစ်ခု သို့မဟုတ် တစ်ခုထက်ပိုပြီး ပါဝင်လို့ရပါတယ်။

<br>

![primary](./assets/img/primary.jpg)

<br>

1. It contains only a unique value.

2. It can not be null.

3. One table can have only one Primary Key.

4. A primary key length cannot be more than 900 bytes.

table တစ်ခုကို primary key ကို single column တွင် ထည့်သွင်း တည်ဆောက်တော့မယ်ဆိုရင်

```sql
    CREATE TABLE IF NOT EXISTS tbname (
                                        colname datatype NOT NULL AUTO_INCREMENT PRIMARY KEY, colname datatype, etc.
                                        );
```

or

```sql
    CREATE TABLE IF NOT EXISTS tbname (
                                        colname datatype NOT NULL AUTO_INCREMENT,
                                        colname datatype, etc., PRIMARY KEY (id);
                                        );
```

table တစ်ခုကို primary key ကို multi column တွင် ထည့်သွင်း တည်ဆောက်တော့မယ်ဆိုရင်

```sql
    CREATE TABLE IF NOT EXISTS tbname (
                                        colname datatype NOT NULL,
                                        colname datatype NOT NULL,
                                        CONSTRAINT keyname PRIMARY KEY(colname, colname)
                                        );
```

ရှိပီးသား column ကို primary key ထည့်ချင်ရင်တော့

```sql
    ALTER TABLE tbname ADD PRIMARY KEY (colname);
```

or

```sql
    ALTER TABLE tbname MODIFY COLUMN colname datatype NOT NULL AUTO_INCREMENT PRIMARY KEY;
```

or

```sql
    ALTER TABLE tbname MODIFY COLUMN colname datatype NOT NULL AUTO_INCREMENT, ADD PRIMARY KEY (colname);
```

ရှိပီးသား multi column ကို primary key ထည့်ချင်ရင်တော့

```sql
    ALTER TABLE tbname ADD CONSTRAINT key_name PRIMARY KEY (col,col,col);
```

ရှိပီးသား primary key ကို ပြန်ဖျက်ချင်တယ် ဆိုရင်တော့ သူမှာ `auto_increment` ပါမပါ တစ်ချက်စစ်ရမယ်။

```sql
    desc tbname;
```

`AUTO_INCREMENT` ပါခဲ့ရင် အရင်ဖြုတ်ပေးရမယ်။

```sql
    ALTER TABLE tbname modify colname datatype NOT NULL;
```

and then

```sql
    ALTER TABLE tbname DROP PRIMARY KEY;
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
