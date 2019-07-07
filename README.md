# springboot-batch-csvtodb

Spring Batch CSV to Database both H2 and Mysql DB insertion 

Conditional bean creation

# For H2 consle
When you start the application, you can launch up H2 Console at http://localhost:8080/h2-console.

Tip - Make sure that you use jdbc:h2:mem:testdb as JDBC URL.

Markup :  - - - -

# H2 or Mysql connectivity
set below property to H2 or MYSQL

domain.datasource.type=MYSQL

Markup :  - - - -

#Spring Batch Count of Processed Records
ItemStream and ChunkListener to count number of records processed by Spring batch job and log the record count in logs file or console.

Markup :  - - - -

# validation using ValidationProcessor
validate Employee data using ValidationProcessor

> ItemProcessor to add business logic after reading the input and before passing it to writer for writing to the file/database. It should be noted that while
> it’s possible to return a different datatype than the one provided as input, it’s not necessary.

Returning null from ItemProcessor indicates that the item should not be continued to be processed.

How to write ItemProcessor
Below given ItemProcessor implementation does following tasks:

* Validate if 'id' field is set.
* Validate if 'id' field is parsable to integer.
* Validate if 'id' field is positive integer greater than zero.
* If validation fails then return null, which indicate that don’t process the record.
* If validation succeeds then return the Employee object, as it is.

