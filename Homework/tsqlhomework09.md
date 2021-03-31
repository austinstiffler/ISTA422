#### T-SQL Chapter 9 Homework
#### Austin Stiffler
#### 23 March, 2021
---

1. A table used to keep a full history of data changes for later analysis.

1. You could use a temporal table to audit data that has changed.

1. 
  * A primary key
  * Two columns defined as DATETIME2 with any precision, which are non-nullable and represent the start and end of the row’s validity period in the UTC time zone
  * A start column that should be marked with the option GENERATED ALWAYS AS ROW START
  * An end column that should be marked with the option GENERATED ALWAYS AS ROW END
  * A designation of the period columns with the option PERIOD FOR SYSTEM_TIME (<startcol>, <endcol>)
  * The table option SYSTEM_VERSIONING, which should be set to ON
  * A linked history table (which SQL Server can create for you) to hold the past states of modified rows

4. Query the current table, but add a clause called FOR_SYSTEM_TIME and a subclause that indicates the validity point or period of time you're interested in.

1. You modify only the current table 
with INSERT, UPDATE, DELETE, and MERGE statements. Behind the scenes, SQL Server updates the period columns and moves 
rows to the history table as needed.

1. Turn off SYSTEM_VERSIONING then use the delete statement.

1. Query the current table, but add a clause called FOR_SYSTEM_TIME and a subclause that indicates the validity point or period of time you're interested in.

1. Use the @start and @end keywords in the query.

1. Turn SYSTEM_VERSIONING off and delete temporal table.