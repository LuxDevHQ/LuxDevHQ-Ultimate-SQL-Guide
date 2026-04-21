### **What is data?**

Data is raw facts or pieces of information. It can be numbers, words, dates, prices, names, marks, phone numbers, or anything we collect and store about people, places, things, or events.

**Examples of data:**
- Amina
- 12
- 2026-04-22
- 4500
- Nairobi

In simple terms, data is the small pieces of information that help us understand something.

**Example:**
- Student name = data
- Student age = data
- Student marks = data

When many pieces of data are collected together, they help us answer questions and make decisions.

### **What Is a Database?**

A database is an organized digital system used to store and manage data so it can be accessed, updated, and used easily.

Think of it as a smart storage place for information. If data is made up of small facts like:
- names
- ages
- phone numbers
- prices
- dates
  
then a database is the place where all those facts are kept in a well-organized way.

**For example, in a school, a database can store:**
- student names
- admission numbers
- classes
- marks
- attendance
- fee balances

Instead of writing everything on paper or putting everything in one messy file, a database keeps the information structured and easy to search.

**Why databases are important:**
- they keep data organized.
- they reduce confusion.
- they make it easy to find specific records.
- they allow updates when information changes.
- they help systems handle large amounts of information.


**Analogy: From the Old Shop Debt Book to Excel and Then to a Database**

Kitambo, many shopkeepers used to record debt in a small notebook. If a customer came and took items without paying immediately, the shopkeeper would write the details by hand.

For example, they might write:

- Mary – bread – KSh 60
- John – sugar – KSh 150
- Peter – milk – KSh 70

Sometimes they would also write the date, but many times they would only write the customer’s name, the item taken, and the amount owed.

This method worked when the shop was still very small, but it came with many problems. Handwriting could be hard to read, some pages could get lost or torn, and it was difficult to summarize anything properly. The shopkeeper could not easily tell who owed the most money, which products were most commonly taken on debt, or which month had the highest sales. The information was there, but it was not easy to use.

Later, some shopkeepers became more organized and started using Excel files instead of notebooks. Now, instead of writing everything in a physical book, they created columns such as:

- customer_name
- item_name
- quantity
- price
- amount_owed
- date

This was a big improvement. Excel made the records look cleaner and more organized. It became easier to total amounts, sort information, filter rows, and check monthly records. The shopkeeper could now answer questions like:

- Who owes the shop money?
- How much debt is still unpaid?
- How much sugar was sold this month?
- Which month had the highest sales?

So Excel was much better than the old debt notebook.

However, as the shop grew bigger, Excel also started showing its limits. The shop now had many customers, many products, daily sales, stock updates, supplier records, debt payments, and restocking history. Everything becoming larger in one file made it harder to manage.

At this stage, the shopkeeper started needing answers to more important business questions such as:

- Which items are on highest demand?
- In which months do people buy more sugar, flour, or cooking oil?
- Which products move fastest?
- Which customers buy most on debt?
- Which products are slow-moving?
- How much stock should be purchased next month?
- Which supplier gives the best prices?

Excel could help to some extent, but when the data became too much, it was no longer the best tool.

That is where a database becomes more useful.

With a database, the shopkeeper no longer keeps everything in one big sheet. Instead, the data is organized properly into separate related tables such as:

- customers
- products
- sales
- debt_records
- payments
- suppliers
- stock

Now the shopkeeper can keep records in a more structured and reliable way. Customer details can be stored in one table, product details in another, daily sales in another, and payments in another. All this information can then be connected and used together.

This makes the records much easier to manage, search, update, and analyze.

The biggest advantage is that the shopkeeper can now query the data. Querying means asking the database questions.

For example, the shopkeeper can ask:

- Show me the most sold products in March
- Show me all customers with unpaid debt
- Show me the total sugar sold in January
- Show me which month had the highest bread sales
- Show me items that are running out of stock
- Show me products that should be restocked soon

This means the shopkeeper is no longer just recording information. They are now using information to make better business decisions.

For example, by looking at past records, the shopkeeper may notice that:

- sugar sells most in December
- bread demand increases at the end of the month
- cooking oil moves faster during school holidays
- some items stay too long on the shelf

This helps the shopkeeper make smarter purchasing decisions. Instead of buying stock by guesswork, they can buy based on real data.

So the journey looks like this:

- Notebook kitambo: good for a very small shop, but messy and hard to analyze
- Excel: more organized and better for calculations, but harder to manage as the business grows
- Database: best for storing large, structured records and answering important business questions

In simple terms, a database helps the shopkeeper move from just writing records to using records to make smart decisions.

**What Is DBeaver?**

DBeaver is a software tool used to work with databases. It gives you a place where you can connect to a database, write SQL queries, run commands, and view results. Instead of typing commands in a more difficult command-line environment, DBeaver provides a friendly interface that makes it easier to see your database, tables, columns, and query output in one place.

In simple terms, if PostgreSQL is the actual database system where data is stored, DBeaver is the application you use to access and manage that database. It helps you open connections, browse tables, insert or edit data, and test SQL queries. This makes it very useful for beginners because they can focus on learning SQL without first struggling with more technical tools.

You can think of DBeaver as a workspace or control panel for databases. It is not the database itself, but it helps you interact with the database easily. For example, in your SQL class, students will use DBeaver to connect to PostgreSQL, create tables, insert records, and run SELECT queries to see data. This is why DBeaver is a good teaching tool for beginners.

