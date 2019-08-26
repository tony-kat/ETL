# **Microsoft SQL Server ETL**


## **Introduction**
This SQL Server ETL serves as a way to take data from two databases and express that data in the new database. It is a way to efficiently consolidate data from these two sources into a single database.


## **Definitions**
**ETL** (*extract, transform, load*): three database functions when combined into a module, pull data from one or multiple database(s) transferring it/them into another database.
- **Extract** is the process of *reading* data from a database. Here, data is usually collected from multiple sources.
- **Transform** is the process of *converting* the extracted data from its previous form into the form suitable for the new database.   
- **Load** is the process of *writing* the data into the target database.



## **Data Sources**
This ETL extracts data from the databases `Database1` and `Database2` and rewrites it in the `GoalDatabase` database.


## **Methods**
The **ETL**'s first look shows a folder titled ***SP*** as well as a schema folder ***CSs*** and a `.gitignore` file. `.gitignore` specifies intentionally untracked files to ignore while the schemas are collections of tables that are under the ownership of one user. These schemas assist in database management and protection. Our ***SP*** folder contains all stored proecedures from both the `Database1` and `Database2` databases, the primary purposes of the ETL are contained here.

Exploring the ***SP*** folder shows us the folders ***1*** and ***2***, as well as two SQL codes that are meant to check the size of a database as well as a code to execute procedures. The ***1*** and ***2*** folders only serve to organize the stored procedures based on which database they are modifying. ***1*** for *Database1* and ***2*** for *Database2*. 

Within the folders, we can see all the standard procedures used to extract data from specific tables within the database.


## **Conclusion**
The application of this SQL Server ETL goes beyond taking data from `Database1` and `Database2` and converting it to be stored in `GoalDatabase`. With proper reformatting, this ETL can be used to take any databases and convert/store that information in another database, utilizing similar organization. Power distribuation as well as modulatity are some of the strngths SQL has, particularly with databases.