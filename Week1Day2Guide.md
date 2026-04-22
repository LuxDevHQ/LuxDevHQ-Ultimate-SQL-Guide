# Week 1 Day 2: SQL For Data ANaluytics

## Tables, Rows, Columns, Data Types, and Schemas

By this point, you already know that data is raw information, a database is where data is stored in an organized way, and DBeaver is the tool we use to connect to PostgreSQL and write SQL queries. On Day 2, we now move deeper into how data is actually arranged inside a database. This lesson is very important because before you can query data, filter data, update data, or analyze data, you must first understand how the data is structured.

Many beginners rush into writing `SELECT` statements without first understanding what they are selecting from. SQL becomes much easier when you first understand the building blocks of a database. These building blocks include tables, rows, columns, data types, and schemas. Once these are clear, later topics such as filtering, sorting, joins, grouping, and table relationships start making much more sense.

---

# 1. What is a table?

A table is a structure inside a database used to store related data in an organized form. It is one of the most important objects in a relational database. A table keeps information about one subject or one type of thing.

For example:

- a `students` table stores student information
- a `products` table stores product information
- a `payments` table stores payment information
- an `employees` table stores employee information

A table is made up of rows and columns. You can think of a table as looking similar to an Excel sheet, because both have rows and columns. However, a database table is much more powerful because it can enforce rules, prevent bad data, connect to other tables, and support fast querying.

A good table should focus on one topic only. This is important because databases are designed to organize information properly. If you mix too many things into one table, the data becomes confusing and difficult to manage.

For example, a `students` table should store student-related information such as names, ages, and contact details. It should not also store supplier details, stock records, or employee payroll data. Those belong in separate tables.

## Example of a simple students table

| student_id | student_name | age | gender | course |
|------------|--------------|-----|--------|--------|
| 1          | Amina        | 21  | Female | SQL    |
| 2          | Brian        | 24  | Male   | Python |
| 3          | Faith        | 22  | Female | SQL    |

This entire structure is called a table.

---

# 2. Why tables are important

Tables are important because they help keep information organized, structured, and easy to manage. Without tables, all data would be mixed together in one messy place.

Imagine a school trying to store:

- student names
- teacher names
- exam scores
- payments
- attendance
- subjects
- classes

If all this information were thrown into one place without structure, it would become very difficult to understand or use. A table solves this by separating data into clear sections.

Tables help us:

- store data properly
- search for specific records
- update information
- delete records when needed
- analyze patterns
- avoid confusion
- prepare data for reports and decisions

So tables are not just containers. They are the main way a database keeps order.

---

# 3. What is a row?

A row is one complete record in a table. It represents one full item, person, event, or entry depending on what the table is about.

In a students table, one row represents one student.  
In a products table, one row represents one product.  
In an employees table, one row represents one employee.

Using the table below:

| student_id | student_name | age | gender | course |
|------------|--------------|-----|--------|--------|
| 1          | Amina        | 21  | Female | SQL    |
| 2          | Brian        | 24  | Male   | Python |
| 3          | Faith        | 22  | Female | SQL    |

Each line of data is a row.

So:

- `1 | Amina | 21 | Female | SQL` = one row
- `2 | Brian | 24 | Male | Python` = one row
- `3 | Faith | 22 | Female | SQL` = one row

A row gives us all the details for one record.

### Simple meaning of a row

A row is one complete entry in the table.

### Real-life examples

- one hospital patient = one row
- one shop product = one row
- one Mpesa transaction = one row
- one employee = one row
- one book in a library = one row

This idea is very important because when you query a table, SQL often returns rows.

---

# 4. What is a column?

A column is one field or one category of information in a table. It describes one property of the records in the table.

In the students table:

- `student_id` is a column
- `student_name` is a column
- `age` is a column
- `gender` is a column
- `course` is a column

Each column stores one type of information about each record.

For example, in a students table:

- the `student_name` column stores student names
- the `age` column stores ages
- the `gender` column stores gender values
- the `course` column stores course names

### Simple meaning of a column

A column is one attribute or one characteristic of the data.

### Real-life examples

If the table is about products, the columns may be:

- product_id
- product_name
- category
- price
- stock_quantity

If the table is about employees, the columns may be:

- employee_id
- full_name
- department
- salary
- hire_date

This means that columns tell us what kind of details we are collecting about each record.

---

# 5. Difference between a row and a column

Students often confuse rows and columns, so this must be very clear.

A row is a full record.  
A column is one piece of information about that record.

## Example

In the following table:

| student_id | student_name | age | gender | course |
|------------|--------------|-----|--------|--------|
| 1          | Amina        | 21  | Female | SQL    |

- the whole line for Amina is one row
- `student_name` is a column
- `age` is a column
- `course` is a column

### Short memory trick

- row = record
- column = field

Another way to remember it:

- rows go across
- columns go down

---

# 6. What is a cell?

A cell is the point where a row and a column meet. It contains one single value.

For example, in the table:

| student_id | student_name | age | gender | course |
|------------|--------------|-----|--------|--------|
| 1          | Amina        | 21  | Female | SQL    |

Examples of cells are:

- `1` under `student_id`
- `Amina` under `student_name`
- `21` under `age`
- `Female` under `gender`
- `SQL` under `course`

A table is made up of many cells, and each cell stores one value only.

This may sound small, but it matters because databases work by storing values in cells, arranged in rows and columns.

---

# 7. Analogy: Admission form

A good way to understand tables, rows, and columns is to think of a student admission form.

The form may ask for:

- full name
- age
- gender
- phone number
- course
- email address

Each question on the form becomes a column in the database.

Then each student who fills the form becomes one row in the table.

So:

- questions on the form = columns
- one completed student form = one row

This is exactly how tables work.

---

# 8. What makes a good table?

A good table should be designed carefully. It should not just hold data; it should hold data in a clear and useful way.

A good table should:

- focus on one subject
- have meaningful column names
- avoid storing unrelated information
- store data in the correct format
- have a primary key
- be easy to read and manage

For example, a table called `students` should not contain columns like:

- supplier_name
- truck_number
- warehouse_location

Those do not belong there because they are not about students.

A well-designed table makes querying easier and reduces mistakes later.

---

# 9. What is a primary key?

A primary key is a column that uniquely identifies each row in a table. It is one of the most important concepts in relational databases.

This means that the value in the primary key column must be unique for every row. No two rows should share the same primary key value.

## Example

| student_id | student_name | age |
|------------|--------------|-----|
| 1          | Amina        | 21  |
| 2          | Brian        | 24  |
| 3          | Faith        | 22  |

Here, `student_id` can be the primary key because each student has a different ID.

### Why not use names as primary keys?

Because names can repeat.

You may have:

- two students called John
- two patients called Mary
- two employees called David

Names are not guaranteed to be unique, but an ID should always be unique.

### Why primary keys are important

Primary keys help because they:

- identify each row clearly
- prevent confusion
- make updates safer
- support relationships between tables
- help avoid duplicate identity problems

If a table has no reliable way to identify each row, managing the data becomes difficult.

---

# 10. What is a duplicate?

A duplicate is repeated information that should not be repeated. Duplicates often create confusion and can cause inaccurate reporting.

## Example

| student_id | student_name | age |
|------------|--------------|-----|
| 1          | Amina        | 21  |
| 1          | Amina        | 21  |

This is a problem because the `student_id` should be unique.

Duplicates can lead to:

- wrong counts
- wrong totals
- confusion during updates
- repeated records in reports

This is one reason why primary keys are very important.

---

# 11. What is NULL?

`NULL` means the value is missing or unknown.

This is very important. `NULL` does not mean zero. It also does not mean an empty string. It means no value has been stored.

## Example

| student_id | student_name | phone_number |
|------------|--------------|--------------|
| 1          | Amina        | 0712345678   |
| 2          | Brian        | NULL         |

Brian’s phone number is missing, so it is `NULL`.

### Important note

`NULL` is not:

- `0`
- `FALSE`
- empty text
- the word `"unknown"`

`NULL` means there is no value stored.

### Why NULL matters

This matters because databases treat `NULL` differently from real values. For example, when filtering or calculating, `NULL` values require special handling.

So students must understand early that missing data is not the same as zero or blank text.

---

# 12. What are data types?

A data type is a rule that tells the database what kind of value a column can store.

This is one of the most important database concepts because not every column should accept every kind of value.

For example:

- a person’s age should store numbers
- a name should store text
- a joining date should store a date
- a salary should store a decimal number
- a yes/no status should store a boolean value

A database uses data types to protect the quality of the data.

### Simple definition

A data type tells the database what kind of information belongs in a column.

---

# 13. Why data types matter

Data types matter because they help the database enforce order and accuracy.

They help with:

- data quality
- storage efficiency
- calculations
- sorting
- filtering
- reducing mistakes

## Example 1: age

If age is stored as text instead of numbers, calculations become harder.

## Example 2: date

If a joining date is stored as random text, sorting dates becomes difficult.

## Example 3: money

If price is stored as text, calculating totals and averages may not work correctly.

So when creating a table, choosing the correct data type is part of good database design.

---

# 14. Common PostgreSQL data types

Below are some of the most common data types students should know at this stage.

## 14.1 INTEGER

`INTEGER` stores whole numbers.

### Examples

- 1
- 25
- 300
- -5

### Use it for

- age
- quantity
- number of books
- marks
- stock count

### Example

```sql
age INTEGER
```

You use INTEGER when you want a number with no decimal places.
