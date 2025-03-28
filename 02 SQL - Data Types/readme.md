[![php](https://img.shields.io/badge/PHP-000?style=for-the-badge—=ko-fi—=white)](#)

> I'm Zaw Linn Tun a Frontend Web Developer on [Zaw Linn - Vlog](https://www.github.com/zawlinn-vlog). :heart:

<!-- #### PROJECT SIMPLE &mdash; -->

<!-- ![PROJECT_IMG](./assets/img/sample.png) -->

<br/>

## SQL Datatype &mdash;

SQL မှာ Store လုပ်နိုင်တဲ့ Data Type တွေက Character (string data)၊ Number (Numeric data)၊ Binary data, Date and time data, Binary Strings စသည်ဖြင့်တို့ ဖြစ်ပါတယ်။ ဒီတော့ ကျတော်တို့ database table ကို ဖန်တီးတဲ့အခါ attribute နှစ်ခုကို ကြိုတင် ကြေငြာပေးမို့ လိုပါလိမ့်မယ်။

- Column ရဲ့ name နှင့်
- Column ရဲ့ datatype ပဲ ဖြစ်ပါတယ်။

## SQL ရဲ့ Data Type များ

SQL မှာ အဓိကအားဖြင့် Data types သုံးမျိုးကို တွေ့နိုင်ပါတယ်။

- String
- Numeric
- Date and Time

### MySQL - String Data Types &mdash;

| Data type       | Description                                                                                                                                                                                                           |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CHAR(size)      | String data type အမျိုးအစားဖြစ်ပီး length ကို fixed လုပ်ထားပါတယ်။ letter, number and special character တွေကို လက်ခံနိုင်ပီး size အနေနဲ့ 0 ကနေ 255 လုံးထိလက်ခံပေးနိုင်ပါတယ်။ Default size က 1 ဖြစ်ပါတယ်။ 8 bytes       |
| VARCHAR(size)   | String data type အမျိုးအစားဖြစ်ပီး length က dynamic ဖိပါတယ်။ letter, number and special character တွေကို လက်ခံနိုင်ပီး size အနေနဲ့ 0 ကနေ 65535 လုံးထိလက်ခံပေးနိုင်ပါတယ်။ - 16 byets becoz 1 charater is 1byte (8bits) |
| BINARY(size)    | CHAR() နဲ့တူတူပဲ ဖြစ်ပါတယ်။ ဒါမဲ့သူကျ binary byte string တွေကို store လုပ်တာဖြစ်ပါတယ် သူရဲ့ lenght ကို byte နဲ့ သတ်မှတ်ပီး Default က 1 ဖြစ်ပါတယ်။                                                                     |
| VARBINARY(size) | VARCHAR() နဲ့တူတူပဲ ဖြစ်ပါတယ်။ ဒါမဲ့သူကျ binary byte string တွေကို store လုပ်တာဖြစ်ပါတယ် သူရဲ့ lenght ကို byte နဲ့ သတ်မှတ်ပီး Default က 1 ဖြစ်ပါတယ်။                                                                  |
| TINYTEXT        | သူရဲ့ maximum length က Character 255 လုံးပဲ ဖြစ်ပါတယ်။                                                                                                                                                                |
| TEXT(size)      | သူရဲ့ maximum length က 65535 bytes ပဲ ဖြစ်ပါတယ်။                                                                                                                                                                      |
| MEDIUMTEXT      | သူရဲ့ maximum length က 16,777,215 characters ပဲ ဖြစ်ပါတယ်။ - 16 MB                                                                                                                                                    |
| LONGTEXT        | သူရဲ့ maximum length က 4,294,967,195 characters ပဲ ဖြစ်ပါတယ်။ - 4GB                                                                                                                                                   |
| TINYBLOB        | သူက small BLOBs( Binary Large Objects)ကို ကိုယ်စားပြုတာ ဖြစ်ပါတယ်။ သူရဲ့ max length က 255 ဖြစ်ပါတယ်။                                                                                                                  |
| BLOG(size)      | သူက BLOBs( Binary Large Objects)ကို ကိုယ်စားပြုတာ ဖြစ်ပါတယ်။ သူရဲ့ max length က 65,535 ဖြစ်ပါတယ်။                                                                                                                     |
| MEDUMBLOG       | သူက Medium BLOBs( Binary Large Objects)ကို ကိုယ်စားပြုတာ ဖြစ်ပါတယ်။ သူရဲ့ max length က 16,777,215 ဖြစ်ပါတယ်။                                                                                                          |
| LOGNBLOG        | သူက LOGN BLOBs( Binary Large Objects)ကို ကိုယ်စားပြုတာ ဖြစ်ပါတယ်။ သူရဲ့ max length က 4,294,967,295 ဖြစ်ပါတယ်။                                                                                                         |

<!-- ENUM(val1, val2, val3, ...) A string object that can contain only one value, chosen from a list of possible values. You can list up to 65535 values in an ENUM list. If a value is inserted that is not in the list, a blank value will be inserted. The values are sorted in the order you enter them
SET(val1, val2, val3, ...) A string object that can have 0 or more values, chosen from a list of possible values. You can list up to 64 values in a SET list -->

### MySQL - Numeric Data Types

| Data type    | Description                                                                                                                                                                                                                                                                                                                                           |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| INT          | ပုံမှန် ဆိုဒ် Interget တစ်ခုဖိပီးတော့ signed နဲ့ unsigned ဆိုပီး နှစ်မျိုးတွေ့နိုင်ပါတယ်။ unsigned အနေနဲ့ဆို 0 to 4294967295 ထိ ဖြစ်ပီ signed အနေနဲ့ဆိုရင် -2147483648 to 2147483647 အထိ အလုပ်လုပ်ပါတယ်။ width အနေနဲ့ 11 digit ထက်ပို၍ သတ်မှတ်နိုင်ပါတယ်။                                                                                             |
| TINYINT      | အရမ်းသေးငယ်သော integer ဖိပြီးတော့ သူ့မှာလည်း signed နဲ့ unsigned ဆိုပီး နှစ်မျိုးတွေ့နိုင်ပါတယ်။unsigned အနေနဲ့ဆို 0 to 256 ထိ ဖြစ်ပီ signed အနေနဲ့ဆိုရင် -128 to 128 အထိ အလုပ်လုပ်ပါတယ်။ width အနေနဲ့ 4 digit ထက်ပို၍ သတ်မှတ်နိုင်ပါတယ်။                                                                                                             |
| SMALLINT     | small integer ဖိပြီးတော့ သူ့မှာလည်း signed နဲ့ unsigned ဆိုပီး နှစ်မျိုးတွေ့နိုင်ပါတယ်။unsigned အနေနဲ့ဆို 0 to 65535 ထိ ဖြစ်ပီ signed အနေနဲ့ဆိုရင် -32768 to 32768 အထိ အလုပ်လုပ်ပါတယ်။ width အနေနဲ့ 5 digit ထက်ပို၍ သတ်မှတ်နိုင်ပါတယ်။                                                                                                                |
| MEDIUMINT    | medium-sized integer ဖိပြီးတော့ သူ့မှာလည်း signed နဲ့ unsigned ဆိုပီး နှစ်မျိုးတွေ့နိုင်ပါတယ်။unsigned အနေနဲ့ဆို 0 to 16,777,215 ထိ ဖြစ်ပီ signed အနေနဲ့ဆိုရင် -8388608 to 8388608 အထိ အလုပ်လုပ်ပါတယ်။ width အနေနဲ့ 9 digit ထက်ပို၍ သတ်မှတ်နိုင်ပါတယ်။                                                                                                |
| BIGINT       | Large integer အမျိုးစား ဖိပြီးတော့ သူ့မှာ signed နဲ့ unsigned ဆိုပီး နှစ်မျိုးတွေ့နိုင်ပါတယ်။unsigned အနေနဲ့ဆို 0 to 18,446,744,073,709,551,615 ထိ ဖြစ်ပီ signed အနေနဲ့ဆိုရင် -9223372036854775807 to 922,337,203,854,775,807 အထိ အလုပ်လုပ်ပါတယ်။ width အနေနဲ့ 20 digit ထက်ပို၍ သတ်မှတ်နိုင်ပါတယ်။                                                    |
| FLOAT(M,D)   | floating-point number အမျိုးအစားဖြစ်ပီးတော့ သူကတော့ unsigned အမျိုးစားထဲ မပါဝင်ပါဘူးခင်ဗျာ length အနေနဲ့ M ဖြင့်ပြသပီး D ကတော့ Decimals ကို ကိုယ်စားပြုတာ ဖြစ်ပါတယ်။ default က 10, 2 width (10 digits and 2 decimal point) ဖြစ်ပီးတော့ float အတွက် decimal precision က 24 places ထိ ထားနိုင်ပါတယ်။                                                    |
| DOUBLE(M,D)  | double percision floating-point number အမျိုးအစားဖြစ်ပီးတော့ သူကတော့ unsigned အမျိုးစားထဲ မပါဝင်ပါဘူးခင်ဗျာ length အနေနဲ့ M ဖြင့်ပြသပီး D ကတော့ Decimals ကို ကိုယ်စားပြုတာ ဖြစ်ပါတယ်။ default က 16, 4 width (16 digits and 4 decimal point) ဖြစ်ပီးတော့ Doble အတွက် decimal precision က 53 places ထိ ထားနိုင်ပါတယ်။ `REAL` is a synonym for `DOUBLE`. |
| DECIMAL(M,D) | unpacked floating-point number အမျိုးအစားဖြစ်ပီးတော့ သူကတော့ unsigned အမျိုးစားထဲ မပါဝင်ပါဘူးခင်ဗျာ။ unpacked decimal မှာ decimal တစ်ခုချင်းဆီဟာ one byte နဲ့ သတ်ဆိုင်ပါတယ်။ `NUMERIC` is a synonym for `DECIMAL`.                                                                                                                                    |

### MySQL - Date and Time Data Types

| Data type | Description                                                                                                                                                                                                                                            |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| DATE      | YYYY-MM-DD format ဖြစ်ပီး, 10000-01-01 ကနေ 9999-12-31 ထိ အလုပ်လုပ်ပါတယ်။ For example, December 30th, 1973 would be stored as 1973-12-30.                                                                                                               |
| DATETIME  | Date and Time ပေါင်းစည်းထားတာ ဖြစ်ပီး YYYY-MM-DD HH:MM:SS format ဖြစ်ပါတယ်။ 1000-01-01 00:00:00 ကနေ 9999-12-31 23:59:59 အထိ အလုပ်လုပ်နိုင်ပါတယ်။ For example, 3:30 in the afternoon on December 30th, 1973 would be stored as 1973-12-30 15:30:00.     |
| TIMESTAMP | datetime format နဲ့ တူပေမဲ့ သူက Hyphens မပါဝင်ပါဘူးခင်ဗျာ။ For example, 3:30 in the afternoon on December 30th, 1973 would be stored as 19731230153000 ( YYYYMMDDHHMMSS )                                                                              |
| TIME      | HH:MM:SS format အတိုင်း အချိန်ကို Store လုပ်ပေးပါတယ်                                                                                                                                                                                                   |
| YEAR(M)   | 2-digits သို့မဟုတ် 4-digit format ကို store လုပ်ပေးပါတယ်။ If the length is specified as 2 (for example YEAR(2)), YEAR can be between 1970 to 2069 (70 to 69). If the length is specified as 4, then YEAR can be 1901 to 2155. The default length is 4. |

> TIMESTAMP :: A timestamp between midnight, January 1st, 1970 and sometime in 2037.

## SQL Operator ဆိုတာ ဘာလဲ &mdash;?

<!-- An SQL operator can be either a unary or binary operator. A unary operator (example unary + or unary - ) uses only one operand to perform the unary operation, whereas the binary operator (example + or - etc) uses two operands to perform the binary operation. -->

SQL operator ဆိုတာ reserved word ဒါမှမဟုတ် SQL statement ရဲ့ WHERE clause နဲ့ တွဲဖက် အလုပ်လုပ်ပါတယ်။ multi conditions တွေကို စစ်ထုတ်တဲ့နေရာမှာ conjunctions သို့မဟုတ် conditions တွေကို လုပ်ဆောင်ပေးနိုင်ပါတယ်။

## Types of Operator in SQL

SQL supports following types of operators:

1. Arithmetic operators
2. Comparison operators
3. Logical operators
4. Operators used to negate conditions

### SQL Arithmetic Operators

SQL Arithmetic Operators တွေကို Numerical Value တွေကို Methematical Operations ပြုလုပ်မို့အတွက် အသုံးပြုပါတယ်။

<!-- SQL Arithmetic Operators are used to perform mathematical operations on the numerical values. SQL provides following operators to perform mathematical operations. -->

Here is a list of all the arithmetic operators available in SQL.

| Operator | Description    | Example        |
| -------- | -------------- | -------------- |
| -        | Addition       | 10 + 20 = 30   |
| \*       | Subtraction    | 20 - 30 = -10  |
| -        | Multiplication | 10 \* 20 = 200 |
| /        | Division       | 20 / 10 = 2    |
| %        | Modulus        | 5 % 2 = 1      |

### SQL Comparison Operators

SQL comparison operator တွေကို expression တွေကို စစ်ဆေးတဲ့အခါ အသုံးပြုပါတယ်။ BOOOLEAN တန်ဖိုးဖိတဲ့ TRUE/FLASE return ပြန်ပေးမှာဖိပီး တခါတရံ Operand တစ်ခုခုရဲ့ value က Null ဖိသွားတဲ့အခါမှာ result က UNKNOWN ဖိသွားနိုင်ပါတယ်။

<!-- SQL Comparison Operators test whether two given expressions are the same or not. These operators are used in SQL conditional statements while comparing one expression with another and they return a Boolean value which can be either TRUE or FALSE. The result of an SQL comparison operation can be UNKNOWN when one or another operand has it's value as NULL. -->

Here is a list of all the comparison operators available in SQL.

| Operator | Description              | Example              |
| -------- | ------------------------ | -------------------- |
| =        | Equal to                 | 5 = 5 returns TRUE   |
| !=       | Not equal                | 5 != 6 returns TRUE  |
| <>       | Not equal                | 5 <> 4 returns TRUE  |
| \>       | Greater than             | 4 > 5 returns FALSE  |
| <        | Less than                | 4 < 5 returns TRUE   |
| \>=      | Greater than or equal to | 4 >= 5 returns FALSE |
| <=       | Less than or equal to    | 4 <= 5 returns TRUE  |
| !<       | Not less than            | 4 !< 5 returns FALSE |
| !>       | Not greater than         | 4 !> 5 returns TRUE  |

### SQL Logical Operators

<!-- SQL Logical Operators are very similar to comparison operators and they test for the truth of some given condition. These operators return a Boolean value which can be either a TRUE or FALSE. The result of an SQL logical operation can be UNKNOWN when one or another operand has it's value as NULL. -->

Here is a list of all the logical operators available in SQL.

| Operator | Description                                                                                 |
| -------- | ------------------------------------------------------------------------------------------- |
| ALL      | TRUE if all of a set of comparisons are TRUE.                                               |
| AND      | TRUE if all the conditions separated by AND are TRUE.                                       |
| ANY      | TRUE if any one of a set of comparisons are TRUE.                                           |
| BETWEEN  | TRUE if the operand lies within the range of comparisons.                                   |
| EXISTS   | TRUE if the subquery returns one or more records                                            |
| IN       | TRUE if the operand is equal to one of a list of expressions.                               |
| LIKE     | TRUE if the operand matches a pattern specially with wildcard.                              |
| NOT      | Reverses the value of any other Boolean operator. Example                                   |
| OR       | TRUE if any of the conditions separated by OR is TRUE                                       |
| IS       | NULL TRUE if the expression value is NULL.                                                  |
| SOME     | TRUE if some of a set of comparisons are TRUE.                                              |
| UNIQUE   | The UNIQUE operator searches every row of a specified table for uniqueness (no duplicates). |

### SQL Operator Precedence

အမျိုးမျိုးသော operator တွေကို SQL မှာ အသုံးပြုသောအခါ operator precedence ပေါ်မူတည်ပီး ဘယ်တစ်ခုကို အရင်ဦးဆုံး လုပ်ဆောင်ရမလဲ ဆိုတာ ဆုံးဖြတ်ပါတယ်။

<!-- The operator precedence in SQL is the sequence in which the SQL evaluates the different operators in a given expression. The operators with higher precedence get evaluated first. -->

Following table lists all SQL operators as per their precedence.

| Operator                                       | Operation                |
| ---------------------------------------------- | ------------------------ |
| +, -                                           | identity, negation       |
| \*, /                                          | multiplication, division |
| +, -                                           | addition, subtraction    |
| =, !=, <, >, <=, >=,IS NULL, LIKE, BETWEEN, IN | Comparison               |
| NOT                                            | logical negation         |
| AND                                            | conjunction              |
| OR                                             | inclusion                |

> The operators with the highest precedence are at the top and the operators with the lowest precedence are at the bottom.

## SQL Command

1. single line Comment

```sql
    -- single line comment
```

2. Multi line Comment

```sql
    /*  Multi
        Line
        Comment
     */
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
