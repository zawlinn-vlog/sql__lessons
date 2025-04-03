[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

## UNIQUE ဆိုတာ ဘာလဲ &mdash; ?

Unique ဆိုတာ ထည့်သွင်းသော Data တွေကို Duplicate မဖြစ်စေလိုသောအခါ unique column တွေ သတ်မှတ်ပေးရမှာ ဖြစ်ပါတယ် ခင်ဗျာ။

> Unique column သည် Snigle or Multiple ဖြစ်နိုင်ပါတယ်။

1. The `unique key` is similar to the `primary key` in a table, but it can accept `NULL` values, whereas the `primary key` does not.

2. It accepts only one NULL value.

3. It cannot have duplicate values.

4. It can also be used as a `foreign key` in another table.

5. A table can have more than one Unique column.

ရှိပီးသား Table ထဲမှာ Single Unique Column သတ်မှတ်ခြင်း

```sql
    ALTER TABLE tbname ADD UNIQUE (colname);
```

ရှိပီးသား Table ထဲမှာ Multi Unique Column သတ်မှတ်ခြင်း

```sql
    ALTER TABLE tbname ADD CONSTRAINT index_name UNIQUE (col, col, etc...)
```

Single Unique Key ပါဝင်တဲ့ Table ကို Create ပြုလုပ်ခြင်း

```sql
    CREATE TABLE IF NOT EXISTS tbname (colname datatype constraint, colname datatype UNIQUE KEY);
```

or

```sql
    CREATE TABLE IF NOT EXISTS tbname (colname datatype constraint, colname datatype, UNIQUE (colname));
```

or

```sql
    CREATE TABLE IF NOT EXISTS tbname (colname datatype constraint, colname datatype, UNIQUE KEY (colname));
```

Multiple Unique Key ပါဝင်တဲ့ Table ကို Create ပြုလုပ်ခြင်း

```sql
    CREATE TABLE IF NOT EXISTS tbname (colname datatype, colname datatype, CONSTRAINT index_name UNIQUE  (colname,colname));
```

Unique Key ကို ပြန်ဖျက်ခြင်း

အရင်ဆုံး `index_name` စစ်ကြည့်မယ်

```sql
    SHOW INDEX FROM tbname;
```

ပီးတဲ့အခါမှ

```sql
    ALTER TABLE tbname DROP INDEX index_name;
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
