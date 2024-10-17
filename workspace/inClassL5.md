## In-Class Task 5: Working with Tables - Alter, Update & Delete

You are required to use the following database [sampleDb.sql](https://dipaish.github.io/databases/sampleDb.sql)

> Note: Before proceeding with the tasks below, create a copy of the database `sampleDb.sql` and name the new database `sampleDbNew` Perform all the following tasks in the `sampleDbNew` database:

### ALTER Table:

1. **Add a new column `courseType` to the `course` table:**  
   Write a query to add a column `courseType` (VARCHAR(10)) to the `course` table.

2. **Modify the `participants` column to allow NULL values:**  
   Write a query to alter the `participants` column to accept NULL values.

3. **Change the data type of `period` to `TINYINT`:**  
   Write a query to change the data type of the `period` column from `SMALLINT` to `TINYINT`.

4. **Drop the `courseType` column from the `course` table:**  
   Write a query to remove the `courseType` column from the `course` table.

5. **Rename the column `startDate` to `beginDate`:**  
   Write a query to rename the `startDate` column to `beginDate`.

6. **Add a default value of 0 for the `participants` column:**  
   Write a query to alter the `participants` column to have a default value of 0.

7. **Add a foreign key constraint on `teacherId` referencing the `teachers` table:**  
   Write a query to add a foreign key constraint on `teacherId` referencing the `teacherId` column in the `teachers` table.

### UPDATE Records:

8. **Update the `participants` for a specific course:**  
   Write a query to update the `participants` to 20 for the course with `subjectId` 'a290' and `period` 1.

9. **Update `teacherId` to `h999` for all courses starting in 2024:**  
   Write a query to update `teacherId` to 'h999' for all courses where the `startDate` is in the year 2024.

10. **Set all `participants` to NULL where `teacherId` is `NULL`:**  
    Write a query to update all courses with `teacherId` set to `NULL` by also setting `participants` to `NULL`.

11. **Increase `participants` by 5 for all courses starting after '2023-01-01':**  
    Write a query to increment the `participants` by 5 for courses with a `startDate` later than '2023-01-01'.

12. **Update the `startDate` for a specific course:**  
    Write a query to change the `startDate` to '2024-05-01' for the course with `subjectId` 'b210' and `period` 2.

### DELETE Records:

13. **Delete a course with a specific `subjectId`:**  
    Write a query to delete the course where `subjectId` is 'a450' and `period` is 2.

14. **Delete all courses with no assigned `teacherId`:**  
    Write a query to remove all courses where the `teacherId` is `NULL`.

15. **Delete all courses that ended before '2023-01-01':**  
    Write a query to delete all courses where the `endDate` is before '2023-01-01'.
