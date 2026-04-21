## **SQL for Absolute Beginners with PostgreSQL and DBeaver.**

---

### What this course is
This is a full beginner SQL course manual for class teaching and self-practice.

### Who this course is for
- Absolute beginners.
- Students who never heard of SQL, PostgreSQL, DBeaver, or databases.
- Teachers who want a complete class guide.

### What students will learn
Students will learn:
- What data is.
- What a database is.
- How to use SQL to create, read, update, and delete data.
- How to use PostgreSQL (local and cloud on Aiven).
- How to use DBeaver as the learning tool.

### Why SQL is useful in today’s world
SQL is used almost everywhere:
- Schools (student records)
- Hospitals (patient visits)
- Banks (transactions)
- Mobile money (wallet balance and transfers)
- Supermarkets (products and sales)
- Social media (users, posts, likes)

If you can use SQL, you can understand and work with real-world data.

### Why PostgreSQL is good for beginners
- Free and powerful.
- Used by real companies.
- Strong, safe, and reliable.
- Great for learning now and using at work later.

### Why DBeaver is good for learning
- Friendly visual interface.
- Helps students connect to databases without fear.
- Lets students write SQL and see results in tables.
- Easy to switch between local PostgreSQL and Aiven cloud PostgreSQL.

---

## Learning Outcomes

By the end of this course, students should be able to:
- Explain data, information, database, table, row, and column in simple words.
- Open DBeaver and connect to a PostgreSQL database.
- Connect to both local PostgreSQL and Aiven PostgreSQL.
- Create databases and tables using PostgreSQL SQL syntax.
- Pick correct data types for columns.
- Use constraints to protect data quality.
- Insert data with `INSERT INTO`.
- Read data with `SELECT`.
- Filter data with `WHERE`, `AND`, `OR`, and more.
- Sort data with `ORDER BY`.
- Update rows with `UPDATE` safely.
- Delete rows with `DELETE` safely.
- Use aggregates like `COUNT()` and `SUM()`.
- Group data using `GROUP BY` and `HAVING`.
- Join multiple tables with `INNER`, `LEFT`, `RIGHT`, and `FULL` joins.
- Use beginner subqueries.
- Create and use views.
- Understand beginner database design and normalization.
- Create simple indexes and understand why they help.
- Build and query a small real-life database project.

---

## Prerequisites

Good news: **No prior knowledge is required**.

You only need:
- Basic computer use (open apps, type text, copy/paste).
- Patience and curiosity.
- Willingness to make mistakes and learn from them.

---

## Teaching Approach

This course uses a teaching style that is:
- **Simple**: easy words, no rushing.
- **Practical**: every idea has examples.
- **Step by step**: one small block at a time.
- **Example-based**: learn by doing.
- **Beginner-friendly**: no shame, no fear.
- **Understanding-first**: know the “why,” not just memorize commands.

Teacher tip: Always ask students to explain ideas back in their own words.

---

## How to Explain SQL to a Child

“Imagine you have many toy boxes.
Each box has a label:
- Cars
- Dolls
- Blocks

Now imagine you ask:
- ‘Show me all red cars.’
- ‘Count how many dolls.’
- ‘Add this new toy.’

That asking language is like SQL. SQL is how we talk to a data toy room.”

Keep repeating:
- SQL is **asking**.
- Database is **storage**.
- Table is **one organized list**.

---

## Full Course Outline

1. Introduction to Data  
2. Introduction to Databases  
3. Database Terminology  
4. What is SQL?  
5. Categories of SQL Commands  
6. Introduction to PostgreSQL  
7. Introduction to DBeaver  
8. Environment Setup  
9. Creating a Database  
10. Creating Tables  
11. Constraints  
12. Inserting Data  
13. Reading Data with SELECT  
14. Filtering Data  
15. Sorting Results  
16. Updating Data  
17. Deleting Data  
18. Aggregate Functions  
19. Grouping Data  
20. Joins  
21. Subqueries  
22. Views  
23. Basic Database Design  
24. Normalization  
25. Indexes  
26. Practice Database Project  
27. Common Beginner Mistakes  
28. Teacher Notes  
29. Practice Exercises  
30. Recap Questions  
31. Mini Quiz Section  
32. Final Summary

---

## 1. Introduction to Data

### What is data?
Data is small pieces of facts.

Examples:
- A student name: `Amina`
- An age: `12`
- A mark: `85`
- A date: `2026-04-21`

### Raw data vs useful information
- **Raw data** = unorganized facts.
- **Information** = data that was organized so it can help decisions.

Example:
- Raw: many numbers like `80, 55, 93, 72`
- Information: “Class average score is 75.”

### Why organizations collect data
Because data helps answer questions:
- Which products sell most?
- Which patients need follow-up?
- Which students need support?

### Practice
1. Write 5 examples of data in a school.
2. Turn raw data into one useful information statement.

### Recap
- Data = facts.
- Information = useful meaning from organized data.

---

## 2. Introduction to Databases

### What is a database?
A database is an organized digital place where data is stored safely.

### Why databases exist
Because big data becomes hard to manage in random files.
Databases help:
- Organize
- Search quickly
- Update safely
- Share with many users

### Difference Between Excel and a Database

| Excel Spreadsheet | Database |
|---|---|
| Great for small lists | Great for small and very large data |
| Easy for manual entry | Better for structured systems |
| Hard when many users edit at once | Supports many users safely |
| Limited relationships | Strong relationships across tables |
| Good for reports | Good for apps, systems, and reports |

### Real-life systems using databases
- Hospital system
- School portal
- ATM/banking system
- Supermarket POS
- Social media platform

### Practice
1. Give 3 reasons a hospital should use a database and not only Excel.
2. Give one case where Excel is still okay.

---

## 3. Database Terminology

| Term | Simple Meaning | Analogy |
|---|---|---|
| Table | One organized data list | One class register book |
| Row | One item in a table | One student line in register |
| Column | One type of detail | “Age” column in register |
| Record | One full row | Full details of one student |
| Field | Single cell value | Student age = 13 |
| Schema | Blueprint/structure | Building plan of data |
| Database Server | Computer running database software | School office that stores all files |
| Query | Question/command to database | “Show all grade 6 students” |
| Relational Database | Database with related tables | Student table linked to class table |
| Relationship | Connection between tables | Student belongs to a class |

Teacher note: Repeat “table = list” and “row = one item” until everyone is comfortable.

---

## 4. What is SQL?

### SQL meaning
SQL stands for **Structured Query Language**.

Simple meaning: SQL is a language used to talk to databases.

### Why SQL matters
With SQL you can:
- Create data structures
- Add data
- Find data
- Change data
- Remove data safely

### Who uses SQL?
- Data analysts
- Software developers
- Backend engineers
- Database administrators
- Business intelligence teams
- Product and operations teams

### Jobs that use SQL
- Data Analyst
- Backend Developer
- Finance Analyst
- Product Analyst
- Reporting Officer

---

## 5. Categories of SQL Commands

| Category | Full Name | Purpose | Examples |
|---|---|---|---|
| DDL | Data Definition Language | Define structure | `CREATE`, `ALTER`, `DROP` |
| DML | Data Manipulation Language | Change data rows | `INSERT`, `UPDATE`, `DELETE` |
| DQL | Data Query Language | Read data | `SELECT` |
| DCL | Data Control Language | Permissions | `GRANT`, `REVOKE` |
| TCL | Transaction Control Language | Manage transactions | `BEGIN`, `COMMIT`, `ROLLBACK` |

### Tiny example
```sql
CREATE TABLE demo (id SERIAL PRIMARY KEY, name VARCHAR(100));
SELECT * FROM demo;
```
Line by line:
- `CREATE TABLE` (DDL): creates structure.
- `SELECT` (DQL): reads data.

---

## 6. Introduction to PostgreSQL

PostgreSQL (say: post-gres-Q-L) is a powerful relational database system.

### Why “relational”?
Because tables can relate (connect) to each other.

### Why PostgreSQL is popular
- Free and open-source.
- Reliable and secure.
- Used in startups and big companies.
- Great documentation and community.

### Why good for learning and work
You learn one strong system and keep using it in real projects.

---

## 7. Introduction to DBeaver

DBeaver is a tool where you can:
- Connect to databases.
- Write SQL.
- Run SQL and view results.

Think of DBeaver as your SQL classroom notebook and calculator in one.

---

## 8. Environment Setup

## How to Open and Use DBeaver

1. Install and open DBeaver.
2. Click **Database > New Database Connection**.
3. Choose **PostgreSQL**.
4. Fill connection details.
5. Click **Test Connection**.
6. Click **Finish**.

### Meaning of connection details
- **Host**: where database lives (house address).
- **Port**: door number to enter service (PostgreSQL default: `5432`).
- **Database name**: specific database inside server.
- **Username**: account name.
- **Password**: secret key.

### Connect to local PostgreSQL
Usually:
- Host: `localhost`
- Port: `5432`
- Database: `postgres` (or your created DB)
- Username: `postgres` (common default)
- Password: your chosen password

### Test connection tips
If test fails:
- Check PostgreSQL service is running.
- Check port is correct.
- Check username/password.
- Check firewall/antivirus not blocking.

## Local PostgreSQL vs Aiven PostgreSQL

| Local PostgreSQL | Aiven PostgreSQL |
|---|---|
| Runs on your own computer | Runs in cloud server |
| Works without internet (on local machine) | Needs internet |
| Good for practice and offline demos | Good for sharing and remote use |
| You manage updates/backups | Provider helps with infrastructure |

### Connect to Aiven PostgreSQL in DBeaver
1. Create PostgreSQL service in Aiven.
2. Copy connection details from Aiven dashboard.
3. In DBeaver, create new PostgreSQL connection.
4. Paste host, port, db, user, password.
5. If SSL is required, enable SSL settings as provided by Aiven.
6. Test connection and save.

Teacher note: Explain cloud like “renting a house” instead of “building at home.”

### Reading Errors Without Fear
If you see an error, breathe.
Errors are teachers.

Read error in 3 steps:
1. **What line failed?** (line number)
2. **What object failed?** (table/column name)
3. **What type of issue?** (syntax, missing table, wrong data type)

Common error idea: “column does not exist” means name spelling mismatch.

---

## 9. Creating a Database

A database is like one big school cabinet. Inside it, many tables can live.

```sql
CREATE DATABASE school_db;
```
Line by line:
- `CREATE DATABASE` tells PostgreSQL to make a new database.
- `school_db` is the name.
- `;` means “command ends here.”

Why it matters: separate work cleanly (school data separate from hospital data).

---

## 10. Creating Tables

A table stores one kind of thing.

Example: `students` table stores student details.

```sql
CREATE TABLE students (
    student_id SERIAL PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    age INTEGER,
    email VARCHAR(150) UNIQUE,
    date_of_birth DATE,
    is_active BOOLEAN DEFAULT TRUE,
    school_fee NUMERIC(10,2),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```
Line by line:
- `CREATE TABLE students (`: make table named students.
- `student_id SERIAL PRIMARY KEY,`: auto-number ID, unique row identity.
- `full_name VARCHAR(100) NOT NULL,`: text up to 100 chars, must have value.
- `age INTEGER,`: whole number.
- `email VARCHAR(150) UNIQUE,`: email text, cannot repeat.
- `date_of_birth DATE,`: stores date only.
- `is_active BOOLEAN DEFAULT TRUE,`: true/false value, default true.
- `school_fee NUMERIC(10,2),`: exact decimal number, e.g., 1500.50.
- `created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP`: date and time when created.
- `);`: close definition and finish command.

### Data types in simple words
- `INTEGER`: whole number.
- `SERIAL`: auto-increasing whole number.
- `VARCHAR(n)`: short text with max length.
- `TEXT`: long text.
- `DATE`: year-month-day.
- `BOOLEAN`: true/false.
- `DECIMAL`/`NUMERIC`: precise decimal numbers.
- `TIMESTAMP`: date plus time.

### NULL and NOT NULL
- `NULL` means no value (unknown or empty).
- `NOT NULL` means value is required.

Common beginner mistake: thinking NULL equals `0` or empty text `''`. It is different.

---

## 11. Constraints

Constraints are safety rules for data quality.

### PRIMARY KEY
One column (or set) that uniquely identifies each row.

### FOREIGN KEY
Connects one table to another table.

### UNIQUE
Prevents duplicate values.

### NOT NULL
Requires a value.

### CHECK
Requires a condition.

### DEFAULT
Gives automatic default value.

```sql
CREATE TABLE courses (
    course_id SERIAL PRIMARY KEY,
    course_name VARCHAR(100) NOT NULL,
    duration_weeks INTEGER CHECK (duration_weeks > 0)
);

CREATE TABLE enrollments (
    enrollment_id SERIAL PRIMARY KEY,
    student_id INTEGER NOT NULL,
    course_id INTEGER NOT NULL,
    enrolled_on DATE DEFAULT CURRENT_DATE,
    CONSTRAINT fk_student
        FOREIGN KEY (student_id)
        REFERENCES students(student_id),
    CONSTRAINT fk_course
        FOREIGN KEY (course_id)
        REFERENCES courses(course_id)
);
```
Line by line highlights:
- `CHECK (duration_weeks > 0)`: no zero/negative duration.
- `FOREIGN KEY (student_id) REFERENCES students(student_id)`: every student_id must exist in students table.
- `DEFAULT CURRENT_DATE`: if date not given, today is used.

Real life analogy: school admission form checks required fields and valid class numbers.

---

## 12. Inserting Data

```sql
INSERT INTO students (full_name, age, email, date_of_birth, school_fee)
VALUES ('Amina Yusuf', 12, 'amina@example.com', '2014-02-10', 1200.00);
```
Line by line:
- `INSERT INTO students (...)`: choose table and columns.
- `VALUES (...)`: values in same order as listed columns.

Multiple rows:
```sql
INSERT INTO courses (course_name, duration_weeks)
VALUES
('Math Basics', 12),
('Science Basics', 10),
('Computer Basics', 8);
```

Common mistakes:
- Wrong order of values.
- Missing quotes for text.
- Missing comma.
- Adding value to wrong data type.

---

## 13. Reading Data with SELECT

```sql
SELECT * FROM students;
```
- `SELECT`: read data.
- `*` means all columns.
- `FROM students`: source table.

```sql
SELECT full_name, age FROM students;
```
- Reads only two columns.

```sql
SELECT full_name AS student_name FROM students;
```
- `AS` gives temporary display label.

```sql
SELECT DISTINCT age FROM students;
```
- `DISTINCT` removes duplicates in result.

```sql
SELECT * FROM students LIMIT 5;
```
- `LIMIT 5` shows only first 5 rows.

---

## 14. Filtering Data

```sql
SELECT *
FROM students
WHERE age >= 12;
```
- `WHERE` filters rows.
- `>=` means greater than or equal.

### Operators and meaning
- `=` equal
- `>` greater than
- `<` less than
- `>=` greater or equal
- `<=` less or equal
- `<>` not equal

```sql
SELECT * FROM students WHERE age >= 10 AND age <= 13;
SELECT * FROM students WHERE age = 12 OR age = 14;
SELECT * FROM students WHERE NOT age = 12;
SELECT * FROM students WHERE age BETWEEN 10 AND 13;
SELECT * FROM students WHERE age IN (10, 11, 12);
SELECT * FROM students WHERE full_name LIKE 'A%';
SELECT * FROM students WHERE full_name ILIKE 'a%';
SELECT * FROM students WHERE email IS NULL;
SELECT * FROM students WHERE email IS NOT NULL;
```
Teacher tip: `LIKE` is case-sensitive in PostgreSQL, `ILIKE` is case-insensitive.

---

## 15. Sorting Results

```sql
SELECT full_name, age
FROM students
ORDER BY age ASC, full_name DESC;
```
- `ORDER BY` controls sorting.
- `ASC` smallest-to-largest / A-Z.
- `DESC` largest-to-smallest / Z-A.
- Multiple columns sort in priority order.

---

## 16. Updating Data

```sql
UPDATE students
SET school_fee = 1300.00
WHERE student_id = 1;
```
- `UPDATE students`: table to change.
- `SET`: new value.
- `WHERE`: which row to change.

⚠️ Danger:
```sql
UPDATE students SET school_fee = 1300.00;
```
Without `WHERE`, all rows are changed.

---

## 17. Deleting Data

```sql
DELETE FROM students
WHERE student_id = 2;
```
- Deletes only selected row.

Safety tips:
1. Run a `SELECT` with same `WHERE` first.
2. Use transactions (`BEGIN`, `ROLLBACK`) during risky edits.

---

## 18. Aggregate Functions

Aggregation means “combine many rows into one summary answer.”

```sql
SELECT
    COUNT(*) AS total_students,
    AVG(age) AS average_age,
    MIN(age) AS youngest,
    MAX(age) AS oldest,
    SUM(school_fee) AS total_fees
FROM students;
```
Line by line:
- `COUNT(*)`: number of rows.
- `AVG(age)`: average age.
- `MIN(age)`: smallest age.
- `MAX(age)`: largest age.
- `SUM(school_fee)`: total fees.

---

## 19. Grouping Data

```sql
SELECT age, COUNT(*) AS student_count
FROM students
GROUP BY age
HAVING COUNT(*) >= 2;
```
- `GROUP BY age`: make one group per age.
- `HAVING`: filter groups after grouping.

Difference:
- `WHERE` filters rows before grouping.
- `HAVING` filters grouped results.

---

## 20. Joins

Why joins? Data is split across tables to reduce repetition.

Example: students in one table, enrollments in another, courses in another.

```sql
SELECT s.full_name, c.course_name
FROM enrollments e
INNER JOIN students s ON e.student_id = s.student_id
INNER JOIN courses c ON e.course_id = c.course_id;
```
- `INNER JOIN`: only matching rows from both sides.

### Join types in words
- `INNER JOIN`: only matches.
- `LEFT JOIN`: all left table rows + matches from right.
- `RIGHT JOIN`: all right table rows + matches from left.
- `FULL JOIN`: all rows from both, matched when possible.

Visual words:
- Inner = overlap only.
- Left = all left bucket + overlap.
- Right = all right bucket + overlap.
- Full = everything from both buckets.

---

## 21. Subqueries

A subquery is a query inside another query.

### Subquery in WHERE
```sql
SELECT full_name
FROM students
WHERE student_id IN (
    SELECT student_id
    FROM enrollments
    WHERE course_id = 1
);
```
Meaning: find students enrolled in course 1.

### Subquery in FROM
```sql
SELECT t.age, t.total
FROM (
    SELECT age, COUNT(*) AS total
    FROM students
    GROUP BY age
) t
WHERE t.total >= 1;
```

---

## 22. Views

A view is a saved query with a name.

```sql
CREATE VIEW student_course_view AS
SELECT s.full_name, c.course_name, e.enrolled_on
FROM enrollments e
JOIN students s ON e.student_id = s.student_id
JOIN courses c ON e.course_id = c.course_id;
```

Query it:
```sql
SELECT * FROM student_course_view;
```
Why useful:
- Simpler for repeated reports.
- Hides complex join logic.

---

## 23. Basic Database Design

Before coding, think.

### Key words
- **Entity**: a thing (Student, Course).
- **Attribute**: detail of thing (student name, age).
- **Relationship**: connection (student enrolls in course).

### Design steps
1. List real-world things.
2. List each thing’s details.
3. Decide how things connect.
4. Create tables based on this map.

---

## 24. Normalization

Normalization means organizing tables to reduce duplicate data.

### Why repeated data is bad
- Wastes space.
- Causes inconsistency.
- Hard to update safely.

### 1NF (First Normal Form)
- No repeating groups.
- One value per cell.

### 2NF (Second Normal Form)
- 1NF plus every non-key column depends on whole key.

### 3NF (Third Normal Form)
- 2NF plus non-key columns depend only on primary key, not on other non-key columns.

Beginner idea: store each fact once, in the right table.

---

## 25. Indexes

An index is like a book index page.
It helps database find rows faster.

```sql
CREATE INDEX idx_students_full_name
ON students(full_name);
```

Why helpful:
- Faster search for frequent lookups.

Caution:
- Too many indexes can slow inserts/updates.

---

## 26. Practice Database Project (Library Database)

### Problem statement
A community library wants to track:
- Members
- Books
- Borrowing history

### Complete Sample Schema

```sql
-- Create tables
CREATE TABLE members (
    member_id SERIAL PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    phone VARCHAR(20) UNIQUE,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE books (
    book_id SERIAL PRIMARY KEY,
    title VARCHAR(150) NOT NULL,
    author VARCHAR(100) NOT NULL,
    category VARCHAR(50),
    published_year INTEGER CHECK (published_year > 0)
);

CREATE TABLE borrows (
    borrow_id SERIAL PRIMARY KEY,
    member_id INTEGER NOT NULL,
    book_id INTEGER NOT NULL,
    borrowed_on DATE DEFAULT CURRENT_DATE,
    returned_on DATE,
    CONSTRAINT fk_member FOREIGN KEY (member_id) REFERENCES members(member_id),
    CONSTRAINT fk_book FOREIGN KEY (book_id) REFERENCES books(book_id)
);
```

Line by line summary:
- `members` keeps member list.
- `books` keeps book catalog.
- `borrows` connects member and book events.

### Sample Inserts

```sql
INSERT INTO members (full_name, phone)
VALUES
('Grace Njeri', '0700000001'),
('John Otieno', '0700000002'),
('Asha Musa', '0700000003');

INSERT INTO books (title, author, category, published_year)
VALUES
('Learning SQL', 'Alan Beaulieu', 'Technology', 2020),
('Little Women', 'Louisa May Alcott', 'Fiction', 1868),
('Clean Code', 'Robert C. Martin', 'Technology', 2008);

INSERT INTO borrows (member_id, book_id, borrowed_on, returned_on)
VALUES
(1, 1, '2026-04-01', NULL),
(2, 2, '2026-04-03', '2026-04-10'),
(1, 3, '2026-04-05', NULL);
```

### Practice Questions
1. Show all books currently not returned.
2. Show each member and total books borrowed.
3. Show technology books only.
4. Show member names with borrowed book titles.

### Solution Queries

```sql
-- 1
SELECT * FROM borrows WHERE returned_on IS NULL;

-- 2
SELECT m.full_name, COUNT(*) AS total_borrowed
FROM borrows b
JOIN members m ON b.member_id = m.member_id
GROUP BY m.full_name;

-- 3
SELECT * FROM books WHERE category = 'Technology';

-- 4
SELECT m.full_name, bk.title
FROM borrows b
JOIN members m ON b.member_id = m.member_id
JOIN books bk ON b.book_id = bk.book_id;
```

---

## 27. Common Beginner Mistakes

- Forgetting semicolon `;` at command end.
- Misspelling keywords (`SELEC` instead of `SELECT`).
- Wrong column/table name.
- Mixing text and number values.
- Forgetting `WHERE` in `UPDATE`/`DELETE`.
- Confusing `NULL` with zero.
- Join with wrong key columns.
- Using `GROUP BY` incorrectly.

Teacher advice: normalize mistake-making as part of learning.

---

## 28. Teacher Notes

### What to emphasize
- SQL is a language to ask data questions.
- Safety with `UPDATE` and `DELETE`.
- Correct naming and clean structure.

### Where students struggle
- Join logic.
- `GROUP BY` and `HAVING`.
- `NULL` behavior.

### Good analogies
- Table = notebook page.
- Row = one person’s line.
- Column = one question on form.
- Foreign key = ID card linking records.

### DBeaver live demo tips
- Type slowly while explaining symbols.
- Run small queries first.
- Show errors and fix them live.

### Engagement tips
- Ask prediction questions before running SQL.
- Celebrate small wins.
- Pair practice: one types, one explains.

---

## 29. Practice Exercises

### Very Easy
1. Create a table called `fruits` with id and name.
2. Insert 3 fruits.
3. Select all fruits.

### Medium Beginner
1. Create `customers` and `orders` tables.
2. Insert at least 5 rows each.
3. Show customers with total orders using `GROUP BY`.

### Challenge
1. Add constraints (`CHECK`, `UNIQUE`, `DEFAULT`).
2. Write a join with filter and sorting.
3. Create a view for a simple report.

---

## 30. Recap Questions

Use these at the end of each module:
1. What is the difference between row and column?
2. Why do we use primary keys?
3. What happens if `WHERE` is missing in `UPDATE`?
4. Why split data into multiple tables?
5. What is the difference between `WHERE` and `HAVING`?

---

## 31. Mini Quiz Section

### Quiz
1. What does SQL stand for?
2. Which command adds new rows?
3. Which clause filters rows?
4. Which join keeps all rows from left table?
5. What does `COUNT(*)` do?

### Answers
1. Structured Query Language.
2. `INSERT INTO`
3. `WHERE`
4. `LEFT JOIN`
5. Counts number of rows.

---

## SQL Symbols and What They Mean

| Symbol | Meaning in SQL | Simple Explanation |
|---|---|---|
| `*` | All columns | “Show me everything” |
| `()` | Grouping/function args | “Details inside brackets” |
| `;` | End of command | “Stop here” |
| `=` | Equal comparison | “Same as” |
| `,` | Separator | “Next item” |
| `'text'` | Text literal | Words must be in quotes |

Teacher tip: explain symbols out loud every time at first.

---

## How to Think Before Writing a Query

Use the 5-question method:
1. What table has the data?
2. What columns do I need?
3. Do I need all rows or filtered rows?
4. Do I need sorting?
5. Do I need grouping or joins?

Then write query in this order:
1. `SELECT`
2. `FROM`
3. `JOIN` (if needed)
4. `WHERE`
5. `GROUP BY`
6. `HAVING`
7. `ORDER BY`
8. `LIMIT`

---

## Final Summary

Amazing work 🎉

You now understand the foundation of databases and SQL:
- You know what data is.
- You know how tables are built.
- You can insert, read, update, and delete data.
- You can filter, sort, group, and join data.
- You can work in DBeaver.
- You can connect to local PostgreSQL and Aiven PostgreSQL.

You are no longer “new to SQL.” You have a strong beginner foundation.
Keep practicing small steps every day. Small steps become big skills.

You can do this. 💪
