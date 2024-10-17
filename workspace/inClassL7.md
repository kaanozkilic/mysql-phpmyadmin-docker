## In-Class Task 7:Functions

You are required to use the following database [sampleDb.sql](https://dipaish.github.io/databases/sampleDb.sql) for the tasks below:

1. **Use the `COUNT()` function to find the total number of courses:**  
   Write a query to count how many courses are present in the `course` table.

2. **Use the `AVG()` function to find the average number of participants:**  
   Write a query to calculate the average number of participants across all courses.

3. **Use the `MAX()` function to find the course with the highest number of participants:**  
   Write a query to retrieve the maximum number of participants in any course.

4. **Use the `MIN()` function to find the earliest course start date:**  
   Write a query to find the earliest `startDate` of any course.

5. **Use the `SUM()` function to calculate the total number of participants across all courses:**  
   Write a query to calculate the total number of participants in the `course` table.

6. **Use the `UPPER()` function to display `subjectId` in uppercase:**  
   Write a query to select all `subjectId` values from the `course` table and convert them to uppercase.

7. **Use the `LOWER()` function to display `teacherId` in lowercase:**  
   Write a query to select all `teacherId` values from the `course` table and convert them to lowercase.

8. **Use the `DATEDIFF()` function to calculate the duration of each course:**  
   Write a query to calculate the number of days between the `startDate` and `endDate` for each course.

9. **Use the `CONCAT()` function to combine `subjectId` and `teacherId`:**  
   Write a query to concatenate `subjectId` and `teacherId` into a single string for each course.

10. **Use the `IFNULL()` function to display 'No teacher' where `teacherId` is NULL:**  
    Write a query to select all courses and replace `NULL` values in the `teacherId` column with the text 'No teacher'.
