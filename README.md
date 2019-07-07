# springboot-batch-csvtodb

Spring Batch CSV to Database both H2 and Mysql DB insertion 

Conditional bean creation

# For H2 consle
When you start the application, you can launch up H2 Console at http://localhost:8080/h2-console.

Tip - Make sure that you use jdbc:h2:mem:testdb as JDBC URL.

# H2 or Mysql connectivity
set below property to H2 or MYSQL

domain.datasource.type=MYSQL

#Spring Batch Count of Processed Records
ItemStream and ChunkListener to count number of records processed by Spring batch job and log the record count in logs file or console.