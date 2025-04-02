[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

## SQL Query ကို လေ့လာခြင်း &mdash; ?

RDBMS ထဲက Data များကို management ပြုလုပ်တဲ့အခါမှာ query များကို အသုံးပြုပါတယ်။

## Database ချိတ်ဆက်ခြင်း &mdash; ?

1. `cmd` ကို ဖွင့်လိုက်ပါ &mdash;

```sh

    mysql -h localhost -P 3306 -u dbuser -p123

```

- -h | --host=localhost is Host - server ရဲ့ ip address လည်း ထည့်လို့ရပါတယ်
- -P | --port=3306 is Port number - Server ရဲ့ Port number ဖြစ်ပါတယ်
- -u | --user=root is dbuser - Server ရဲ့ system user ဖြစ်ပါတယ်
- -p | --password=123 is dbpass - Server ရဲ့ password ဖြစ်ပါတယ်

## mySQL Client Programs &mdash;

|  #  | Command     | Descriptions                                    |
| :-: | ----------- | ----------------------------------------------- |
|  1  | mysql       | The MySQL Command-Line Client                   |
|  2  | mysqladmin  | A MySQL Server Administration Program           |
|  3  | mysqlcheck  | A Table Maintenance Program                     |
|  4  | mysqldump   | A Database Backup Program                       |
|  5  | mysqlimport | A Data Import Program                           |
|  6  | mysqlshow   | Display Database, Table, and Column Information |
|  7  | mysqlslap   | A Load Emulation Client                         |

## Database တည်ဆောက်ခြင်း &mdash; ?

DDL - Data Definition Language လို့ခေါ်တဲ့ statement ကို အသုံးပြု၍ Database ကို Create လုပ်ပေးပါတယ်။ အကရ်၍ လူကြီးမင်းတို့က Unix or Linux OS ကို အသုံးပြုသူဆိုရင် sql keyword တွေဟာ case-insensitive ဖိပေမဲ့ Database name တွေတော့ case-sensitive ဖိနိုင်ပါတယ်။ အကရ်၍ windows အသုံးပြုသူအတွက်တော့ ဒီ rule က apply ဖိမှာမဟုတ်ပါဘူး ခင်ဗျ။

Database name တွေဟာ valid identifiers, number, letter သို့မဟုတ် underscores ပါဝင်နိုင်ပေမဲ့ Database keyword တွေ ဖိနေလို့တော့ မရပါဘူး ခင်ဗျာ။

<!-- The CREATE DATABASE statement is a DDL (Data Definition Language) statement used to create a new database in SQL. If you are creating your database on Linux or Unix, then database names are case-sensitive, even though SQL keywords are case-insensitive. If you are working on Windows then this restriction does not apply.

Here, the DatabaseName is the name of the database that we want to create. The database name can contain any valid identifiers, such as number, letters, or underscores. But a DatabaseName cannot be a keyword available in SQL.



-->

1. ပထမဦးဆုံးအနေနဲ့ အသုံးပြုမည့် Database ကို တည်ဆောက်ရမယ် ဆိုပါက။

2. မတည်ဆောက်ခင်အရင် DATABSE ကို စစ်ဆေးရပါတယ်။

```sql

    SHOW DATABASES;

```

ပီးနောက် Database တည်ဆောက်ရန်အတွက် &mdash;

```sql

    CREATE DATABSE dbname;

```

or

```sql

    CREATE DATABASE IF NOT EXISTS dbname CHARACTER SET utf8 COLLATE utf8_genteral_ci;

```

## Databse ကို ပြန်ဖျက်ခြင်း &mdash;

တည်ဆောက်ထားသော Database ကို ပြန်ဖျက်ချင်သော အခါ

```sql

    DROP DATABASE dbname;

```

or

```sql
    DROP DATABASE IF EXIST dbname;
```

## Database ကို နာမည် ချိန်ခြင်; &mdash;

တည်ဆောက်ထားသော Database ကို နာမည်ချိန်ချင်သော အခါ

```sql

    RENAME DATABASE oldname TO newname;

```

> RENAME DATABASE ကို Security risk ကြောင့် Version အသစ်မှာ အသုံးပြု၍ မရတော့ပါ ခင်ဗျ။ ထိုကြောင့် databse ကို backup ပြုလုပ်၍ အသစ်ပြန်လည်း ထည့်သွင်းပေးရမှာ ဖြစ်ပါတယ်။

ပထမဆုံးအနေနဲ့ database ကို backup ပြုလုပ်ရမှာ ဖြစ်ပါတယ်။

```sh

    mysqldump -u dbuser -p existingdbname > backdbname.sql

```

ပီးနောက် ရှိနေသော Database ကို ဖျက်ပါ

```sh
    mysqladmin -u dbuser -p drop existingdbname
```

or

```sql
    mysql -u dbuser -p
    DROP DATABSE dbname;
```

ပီးနောက် Database ကို ထားလိုသော name အသစ်ဖြင့် တည်ဆောက်ပါ

```sql
    CREATE DATABASE dbname CHARACTER SET utf8 COLLATE utf8_general_ci;
```

ပီးနော် backup လုပ်ထားသော database ကို ပြန်ထည့်သွင်းရမည်

```sh
    mysqladmin -u dbuser -p buildingdbname < backdbname.sql
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
