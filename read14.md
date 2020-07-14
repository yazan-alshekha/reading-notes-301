# DAtabase Normalization

## Introduction to Database Normalization

Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included. Take a spreadsheet containing the information as an example, where the data contains salespeople and customers serving several purposes:


- Identify salespeople in your organization
- List all customers your company calls upon to sell a product
- Identify which salespeople call on specific customers.

By limiting a table to one purpose you reduce the number of duplicate data contained within your database. This eliminates some issues stemming from database modifications.
To achieve these objectives, we’ll use some established rules. As you apply these rules, new tables are formed. The progression from unruly to optimized passes through several normal forms

There are three normal forms most databases adhere to using.  As tables satisfy each successive database normalization form, they become less prone to database modification anomalies and more focused toward a sole purpose or topic. Before we move on be sure you understand the definition of a database table.

## Reasons for Database Normalization
There are three main reasons to normalize a database.  The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries. 
As we go through the various states of normalization we’ll discuss how each form addresses these issues, but to start, let’s look at some data which hasn’t been normalized and discuss some potential pitfalls. 
I think once you understand the issues, you better appreciate normalization. Consider the following table:

![](https://www.essentialsql.com/wp-content/uploads/2014/06/FirstNormalFormUnormalized-1.png?ezimgfmt=ng:webp/ngcb3)

Note: The primary key columns are underlined

1. The first thing to notice is this table serves many purposes including:

2. Listing the sales offices and phone numbers

3. Associating a salesperson with an sales office

4. Showing each salesperson’s customers

As a DBA this raises a red flag.  In general I like to see tables that have one purpose.  Having the table serve many purposes introduces many of the challenges; namely, data duplication, data update issues, and increased effort to query data.

**Data Duplication and Modification Anomalies**

Notice that for each SalesPerson we have listed both the SalesOffice and OfficeNumber. There are duplicate salesperson data. Duplicated information presents two problems:

1. It increases storage and decrease performance.

2. It becomes more difficult to maintain data changes


