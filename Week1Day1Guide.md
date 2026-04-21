# Week 1 Day 1 Guide: SQL Class Starter (Absolute Beginners)

Welcome to Day 1 🎉  
This guide helps a teacher run the **first SQL lesson** with students who have never heard of SQL, databases, PostgreSQL, or DBeaver.

This lesson is designed to feel:
- safe
- slow
- friendly
- practical
- confidence-building

---

## 1) Day 1 Big Goal

By the end of this first class, students should be able to say:

1. “I know what data is.”
2. “I know what a database is.”
3. “I know what SQL is used for.”
4. “I can open DBeaver and connect to PostgreSQL.”
5. “I can run my first `SELECT` query.”

Teacher reminder: Day 1 is about **comfort first**, not speed.

---

## 2) Suggested Lesson Duration (2 Hours)

| Time | Activity |
|---|---|
| 0:00 - 0:10 | Warm welcome + class rules |
| 0:10 - 0:25 | What is data? (everyday examples) |
| 0:25 - 0:40 | What is a database? |
| 0:40 - 0:55 | What is SQL? |
| 0:55 - 1:10 | Break + Q&A |
| 1:10 - 1:35 | DBeaver + PostgreSQL setup |
| 1:35 - 1:55 | First SQL commands live demo |
| 1:55 - 2:00 | Recap + mini quiz + homework |

---

## 3) Teacher Mindset for Day 1

Tell students:
- “It is okay not to know anything yet.”
- “Mistakes are normal.”
- “Errors are clues, not enemies.”
- “We are learning one brick at a time.”

Use this sentence often:
> “You are not behind. You are learning.”

---

## 4) Warm-Up Script (Teacher Can Read This)

“Today we start from zero. That is perfect.  
No one needs to pretend.  
No one needs to rush.  
Our job today is simple: understand what data is, what a database is, and type our first SQL safely.”

---

## 5) What Is Data? (Simple, Slow Explanation)

### Definition
**Data** is small pieces of facts.

### Easy examples
- A name: `Mary`
- A number: `17`
- A date: `2026-04-21`
- A yes/no answer: `TRUE`

### Everyday places with data
- School attendance sheet
- Hospital patient cards
- Bank transfer list
- Supermarket product list
- Phone contact list
- Library book register

### Why data matters
Data helps people make decisions.

Example:
- Data: many exam scores.
- Decision: which students need extra help.

### Quick class activity
Ask students to list 5 data items from their own day.

---

## 6) What Is a Database?

### Definition
A **database** is an organized digital place for storing data.

### Child-like analogy
Imagine a big cupboard with many labeled drawers:
- Drawer 1: Students
- Drawer 2: Courses
- Drawer 3: Fees

That cupboard is like a database.

### Why not only Excel?
Excel is useful, but databases are better when:
- data becomes big
- many users work together
- relationships are needed
- data safety is important

---

## 7) Core Words for Day 1 (Must Teach Slowly)

| Word | Simple Meaning | Real-Life Picture |
|---|---|---|
| Table | A list | Student register page |
| Row | One item in the list | One student line |
| Column | One type of detail | Name column |
| Query | A question to data | “Show all age 12 students” |
| Database | Organized data home | Cupboard with drawers |
| SQL | Language to ask database | Special question language |

Teacher tip: Ask students to repeat each word with their own example.

---

## 8) What Is SQL?

### Definition
SQL means **Structured Query Language**.

### Super simple meaning
SQL is how we “talk” to a database.

### What SQL can do
- Create tables
- Add rows
- Show rows
- Change rows
- Delete rows

### “What and why”
- **What**: A command language.
- **Why**: So we can control and understand stored data.

---

## 9) SQL Symbols for Day 1

| Symbol | Meaning | How to Explain |
|---|---|---|
| `*` | all columns | “Everything in this list” |
| `;` | end of command | “I finished speaking” |
| `,` | separator | “Next item” |
| `' '` | text wrapper | “Words go inside quotes” |
| `()` | grouped details | “Details inside brackets” |
| `=` | equal | “Same as” |

Mini practice: ask students to read `SELECT * FROM students;` out loud.

---

## 10) Environment Setup (Local PostgreSQL + DBeaver)

### Step A: Open PostgreSQL service
- Ensure PostgreSQL is installed.
- Ensure service is running.

### Step B: Open DBeaver
- Launch DBeaver application.
- Click **Database** → **New Database Connection**.

### Step C: Choose PostgreSQL
- Select PostgreSQL from driver list.

### Step D: Fill connection values
Common local values:
- Host: `localhost`
- Port: `5432`
- Database: `postgres`
- Username: `postgres`
- Password: (the one set during install)

### Step E: Test connection
- Click **Test Connection**.
- If green/success: click **Finish**.

### Common setup issues
1. Wrong password.
2. PostgreSQL service stopped.
3. Wrong port.
4. Typing mistakes in database name.

Teacher live demo rule: show one failure and how to fix it calmly.

---

## 11) Connecting to Aiven PostgreSQL (Cloud)

### Explain cloud simply
Cloud means database is on another computer on the internet.

### Aiven connection steps
1. Create PostgreSQL service in Aiven dashboard.
2. Copy host, port, database, username, password.
3. In DBeaver create PostgreSQL connection.
4. Paste details.
5. Enable SSL settings if Aiven requires.
6. Test and finish.

### Local vs Aiven short explanation
- Local = database on your machine.
- Aiven = database on remote internet machine.

---

## 12) First SQL Commands (Day 1 Hands-On)

### 1. Create a table
```sql
CREATE TABLE students (
    id SERIAL PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    age INTEGER
);
```
Line by line:
- `CREATE TABLE students (`: create a new table named students.
- `id SERIAL PRIMARY KEY,`: automatic id number and unique row key.
- `full_name VARCHAR(100) NOT NULL,`: required text field.
- `age INTEGER`: whole number age.
- `);`: end table creation.

### 2. Insert data
```sql
INSERT INTO students (full_name, age)
VALUES
('Amina', 12),
('Brian', 13),
('Chao', 12);
```
Line by line:
- `INSERT INTO students (full_name, age)`: choose table and columns.
- `VALUES`: provide row values.
- Each `( ... )` is one row.

### 3. Read all data
```sql
SELECT * FROM students;
```
Line by line:
- `SELECT`: read data.
- `*`: all columns.
- `FROM students`: from students table.

### 4. Read filtered data
```sql
SELECT full_name, age
FROM students
WHERE age = 12;
```
Line by line:
- `SELECT full_name, age`: only these columns.
- `FROM students`: data source.
- `WHERE age = 12`: only rows where age is 12.

---

## 13) Class Flow for Live Demo

1. Teacher types SQL slowly.
2. Students predict output before execution.
3. Run query.
4. Compare prediction vs result.
5. Ask: “What changed when we added WHERE?”

This builds understanding, not memorization.

---

## 14) Beginner Mistakes to Expect on Day 1

- Missing semicolon `;`
- Misspelling `SELECT`
- Wrong table name (e.g., `student` vs `students`)
- Using double quotes for text values
- Forgetting commas between values

How to respond as teacher:
- Thank the student for trying.
- Show how to read the error message.
- Fix one thing at a time.

---

## 15) Reading Errors Without Fear (Day 1 Version)

Use the 3-question method:
1. What command failed?
2. What word is highlighted by error?
3. What tiny fix can we try first?

Tell students:
> “Error messages are instructions, not punishment.”

---

## 16) Micro Exercises (In-Class)

### Very Easy
1. Create a table called `fruits` with `id`, `name`, `color`.
2. Insert 3 fruits.
3. Select all fruits.

### Easy-Medium
1. Filter fruits where color is `red`.
2. Show only `name` column.

### Challenge
1. Add one more fruit.
2. Update one fruit color.
3. Delete one fruit row by id.

---

## 17) Day 1 Recap Questions

Ask these before class ends:
1. What is data?
2. What is a database?
3. What does SQL do?
4. What does `SELECT *` mean?
5. Why is `WHERE` useful?

---

## 18) Day 1 Mini Quiz (with Answers)

### Questions
1. SQL stands for what?
2. Which command reads data?
3. Which symbol ends a SQL command?
4. In `WHERE age = 12`, what does `=` mean?
5. What does `*` mean in `SELECT *`?

### Answers
1. Structured Query Language.
2. `SELECT`
3. `;`
4. Equal to.
5. All columns.

---

## 19) Teacher Reflection Checklist (After Class)

- [ ] Did students speak at least once?
- [ ] Did we define every new word clearly?
- [ ] Did we run at least 3 SQL commands together?
- [ ] Did we normalize mistakes?
- [ ] Did students leave with confidence?

---

## 20) Suggested Homework for Students

1. Recreate `students` table at home.
2. Insert 5 student names and ages.
3. Run:
   - `SELECT * FROM students;`
   - `SELECT full_name FROM students;`
   - `SELECT * FROM students WHERE age = 12;`
4. Write one sentence: “Today I learned ______.”

---

## 21) Optional Day 1 Extension (If Class Is Fast)

Introduce two new commands very gently:

```sql
UPDATE students
SET age = 14
WHERE full_name = 'Brian';
```

```sql
DELETE FROM students
WHERE full_name = 'Chao';
```

Important safety reminder:
- Never run `UPDATE` or `DELETE` without `WHERE` on Day 1.

---

## 22) Confidence Closing Script (Teacher Can Read)

“Today you started from zero and wrote real SQL.  
That is a big win.  
You are building a strong foundation.  
Next class will be easier because today you learned the core language.”

---

## 23) Day 1 Quick Reference Card

### Core Commands
```sql
-- Create a table
CREATE TABLE students (
    id SERIAL PRIMARY KEY,
    full_name VARCHAR(100) NOT NULL,
    age INTEGER
);

-- Insert rows
INSERT INTO students (full_name, age)
VALUES ('Amina', 12);

-- Read rows
SELECT * FROM students;

-- Filter rows
SELECT * FROM students WHERE age = 12;
```

### Safety Rules
- Always end commands with `;`
- Check table/column names carefully
- Read errors slowly
- Stay calm and retry

---

## 24) Notes for Next Class (Week 1 Day 2 Preview)

Next class can cover:
- More `SELECT`
- `ORDER BY`
- `DISTINCT`
- `LIMIT`
- More practice with `WHERE`

Tell students this:
> “If Day 1 made sense, Day 2 will feel exciting.”

---

## Final Encouragement

Dear student, if you reached here, you did amazing work.  
Learning SQL is like learning a new way to ask clear questions.  
You now know the first important steps. Keep going. 🌟
