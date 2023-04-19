## Spring 6 Paging and Sorting
##  Paging in Sql
- By default most SQL database will not sort data
- Most GUI tools will set a default limit
- Large record sets can become problematic for performance and memory utilization
- Large meaning hundreds of thousands or millions of records
- In SQL the limit clause is used to limit the number of records returned
- In SQL the offset clause is used to move the starting point of the record set
##  Sort in Sql
- By default most SQL databases will not sort data
- When no sort is specified the order returned is not guaranteed to be the same query to
query
- Often the order will be the same, but beware it can change!
- Sorting is controlled by via the SQL order by clause
- One or more columns can be specified with sort order (asc or desc)
- Default order is ascending 
## Paging and Sorting with Spring Data JPA
- Spring Data JPA provides robust support for paging and sorting
- Spring Data JPA does not have a default limit on records returned
- Spring Data JPA does not set a default sort 
- Only limit is memory of the JVM
- Returning several million records in a JSON response will consume a lot of memory
- Possibly crashing the application
- Best practice is to set default limits for the number of records returned