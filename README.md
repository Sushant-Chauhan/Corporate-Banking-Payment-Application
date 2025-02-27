
# Unit of Work
 
This project implements a Unit of Work (UOW) pattern in Go, providing a convenient way to encapsulate a set of database operations within a single transaction when the Repository pattern is used.
 
The Unit of Work allows to register repositories and perform operations on them, ensuring that all actions are executed within the same transaction.
 
 
### Usage
To use the UOW, follow these steps:
 
1. Import the package into the Go file:
```go
import "github.com/sesaquecruz/go-unit-of-work/uow"
```
3. Create an instance passing a db connection (*sql.DB):
 
```go
UOW := uow.NewUnitOfWork(db)




DB DIAGRAM LINK : https://dbdiagram.io/d/6718af2197a66db9a3f75c8e
```
4. Register the repositories using the Register method:
 
5. Perform database operations within a single transaction by calling the Do method:
 
If an error occurs, the transaction is rolled back and the error is returned. Otherwise, the transaction is committed, and nil is returned.

