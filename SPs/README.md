# **Procedures**


## **Introduction**
The procedures of this ETL are organized into folders based on database names. The goals of these procedures are to transfer and load the data from the original database into the goal database. It can be thought of as where in the entire ETL process the functions are stored. The procedures for this ETL will mainly be moving data around from database to database, but it is important to note that procedures can also run programs/conditional statements/basically anything in a streamlined process. Think of procedures as a list of steps to get from your initial state to your goal state.


## **Definitions**
A *stored procedure* is prepared code that you can save, so the code can beexecuted in another server. You can also pass parameters to a procedure, so that the stored procedure can act based on the parameter value(s) that is passed.


## **Data Sources**

The SP folder contains all of the procedures that the program uses. These procedures are written once and can be called upon in future projects to save time. In addition to these procedures, we also have two codes that stand alone in the SP folder: `check_db_size.sql` and `execute_SPs.sql`. These two codes check the database size as well as execute the procedures respectively. It is important to note that these two codes are *not* procedures.

## **Methods**
All procedures follow the same format when writing the initialization code, that code goes as follows:

```
USE GoalDatabase;
GO
DROP PROCEDURE name_of_procedure;
GO
CREATE PROCEDURE name_of_procedure
AS
```

The program always begins by dropping and creating the procedure to ensure that it has a clean slate to work off of. We discussed this in the schema README.

After creation, the procedures take the tables we had created, and begin to move data included in those tables from a database, to a temporary database which acts as a middle man for the entire process. The data is moved to a temp table in order to keep original databeses available to other collaborators within the original database.

Once the data is fully transferred to the temp database it begins the load into `GoalDatabase`


## **Conclusion**

Stored procedures allow us to consolidate long lines of code into single commands in order to complete the final steps of the entire ETL process. Although their task seems simple, it is a crucial step in defining and maintaining processes.