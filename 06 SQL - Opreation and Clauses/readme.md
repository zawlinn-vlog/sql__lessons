[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

#### WHERE Clauses ကို အသုံးပြုခြင်း

SQL မှာ WHERE ကို result ‌တွေ SELECT, UPDATE သို့မဟုတ် DELETE ပြုလုပ်ရန်အတွက် အသုံးပြုပါတယ်။ ဒါအပြင် multiple table တွေကို Join ပီး record တွေကိုလည်း ထုတ်ပေးနိုင်ပါတယ်။

```sql
    SELECT * FROM tbname WHERE [condition];
```

or

```sql
    SELECT col, col, etc. FROM tbname WHERE [condition];
```

> You can specify a condition using the comparison or logical operator such as, >, <, =, LIKE, NOT, etc.

#### WHERE Clause with IN Operator

ရှာလိုသော value ရှိသည့် record ကို ဆွဲထုတ်တဲ့အခါ WHERE -- IN Operator ကို အသုံးပြုပါတယ်။

```sql
    SELECT col, col, etc. FROM tbname WHERE col IN ('val', 'val', 'val');
```

#### WHERE Clause with NOT IN Operator

ရှာလိုသော value ရှိသည့် record ကို ဖယ်၍ ကျန်သော record များကို ဆွဲထုတ်တဲ့အခါ WHERE -- NOT IN Operator ကို အသုံးပြုပါတယ်။

```sql
    SELECT col, col, etc. FROM tbname WHERE col NOT IN ('val', 'val', 'val');
```

#### WHERE Clause with AND, OR Operator

တစ်ခုထက် ပိုသော condition တွေကို စစ်ထုတ်တဲ့အခါမှာ AND and OR ကို ခြားခံအနေဖြင့် ဆက်ပေးရပါတယ် ခင်ဗျာ။

```sql
    SELECT col, col, etc. FROM tbname WHERE (condition AND condition) OR condition;
```

#### DISTINCT Keyword

ထပ်နေတဲ့ value တွေရှိတဲ့ column ကို distinct သုံးပီး စစ်ထုတ်တဲ့အခါ unique data ကိုသာ တွေ့ရမှာ ဖြစ်ပါတယ်။

```sql
    SELECT DISTINCT col, col, col, etc. FROM tbname | ORDER BY colname | WHERE [condition];
```

### GROUP BY Keyword

Database ထဲက record တွေကို ဆွဲထုတ်တဲ့အခါမှာ column တစ်ခုတည်းမှာ တည်ရှိသော တူညီသော data တွေကို စုစည်းပြီး ထုတ်ယူလို့ပါတယ် ခင်ဗျာ။ သူနဲ့ တွဲသုံးရတဲ့ function တွေရှိပါတယ်။ SUM(), COUNT(), AVG(), MAX(), MIN() and etc.

ဥပမာ - address တူနေတဲ့ record ဘနှခုရှိလဲ သိချင်တဲ့အခါမျိုး

```sql
    SELECT address, count(address) FROM dbname GROUP BY address;
```

> စုစည်းပီး ဆွဲထုတ်ထားတဲ့ record တွေကို filter လုပ်ချင်တဲ့အခါ HAVING ကို အသုံးပြုရပါတယ် WHERE clause သုံး၍ မရတော့ပါ။

```sql
    SELECT age, COUNT(name) FROM dbname GROUP BY age HAVING age > 24;
```

or

```sql
    SELECT age, COUNT(name) FROM dbname GROUP BY age HAVING age > 24 ORDER BY age ASC|DESC;
```

or

```sql
    SELECT age, COUNT(age) FROM dbname GROUP BY age HAVING COUNT(age) >= 2;
```

#### LIKE Operator

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
    SELECT colname FROM dbanme WHERE colname LIKE 'z%';
```

or

```sql
    SELECT colname FROM dbanme WHERE colname LIKE '_un';
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
