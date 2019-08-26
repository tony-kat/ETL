# **Schemas**


## **Introduction**
The schemas within this Miscrosoft SQL Server ETL are collections of tables that contain all of the information needed to run the ETL as well as the field's respective datatypes. This prevents data from being added to those tables that arent in the dataype structures. This allows further procedures to be created with a defined endpoint.


## **Definitions**
A *schema* in a SQL database is a collection of logical structures of data. The schema is owned by a *database user* which grants unique abilities to the owner such as password protection and management. 


## **Data Sources**
Each database (`Database1`,`Database2`) has its own schema associated with it.


## **Methods**
Each schema contains a unique set of tables that analyze certain fields and data types of that specified database. Here, we can see the full schema for `Database1`.
![DS Schema Screenshot](media/Safe_database_Screenshot.png)

It is important to see the actual process the code takes in order to create these schemas. Note that schemas in relative subjects do not differ at all in the syntax; so creating a table schema for `Database2` follows the same format as the table for `Database1`.

This schema begins with the final database this schema will store its information in as well as instructions to drop all specified tables within the database. This is because a table will not be created if it already exists in the database.
```
USE GoalDatabase;
GO
DROP TABLE Database2.Table1
DROP TABLE Database2.Table2
DROP TABLE Database2.Table3
DROP TABLE Database2.Table4
DROP TABLE Database2.Table5
DROP TABLE Database2.Table6
DROP TABLE Database2.Table7
DROP TABLE Database2.Table8
DROP TABLE Database2.Table9
DROP TABLE Database2.Table10
DROP TABLE Database2.Table11
DROP TABLE Database2.Table12
DROP TABLE Database2.Table13
DROP SCHEMA Database2;
GO
CREATE SCHEMA Database2;
GO
```
Once dropped, the script proceeds to create the main schema, thus starting the process of creating the tables.

The script creates a table by listing the name of the table, followed by the field variables and datatypes of those fields:
```
GO

CREATE TABLE Database2.Table (
    FieldVar1	   DataType
,	FieldVar2      DataType
,	FieldVar3	   DataType	
,	FieldVar4      DataType
,	FieldVar5      DataType
,	FieldVar6      DataType
,	FieldVar7      DataType
,	FieldVar8      DataType
,	FieldVar9      DataType
,	FieldVar10     DataType
)
```

This process repeats with every table until the final table is completed, thereby defining the schema. 




## **Conclusion**
Using schemas is the first step toward organizing and preparing data from multiple databases to be transformed into a new set of data for the final database. It is a necessary step for all types of ETL's due to its assistance in organization and protection.