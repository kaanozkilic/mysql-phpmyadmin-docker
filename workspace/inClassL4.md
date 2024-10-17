## In-Class Task 4: Working with Tables - Select & Operators

You are required to use the following database [sampleDb.sql](https://dipaish.github.io/databases/sampleDb.sql) for the tasks below:

1. **Select all records from the `course` table:**  
   Write a query to select all columns and rows from the `course` table.

2. **Select courses with more than 5 participants:**  
   Write a query to retrieve courses where the number of participants is greater than 5.

3. **Select courses that have no assigned teacher:**  
   Write a query to select all courses where `teacherId` is `NULL`.

4. **Select courses starting after '2024-01-01':**  
   Write a query to retrieve all courses where the `startDate` is after '2024-01-01'.

5. **Select courses with participants between 3 and 8:**  
   Write a query to find all courses that have between 3 and 8 participants, inclusive.

6. **Select courses for a specific teacher:**  
   Write a query to retrieve all courses taught by the teacher with `teacherId` 'h123'.

7. **Select courses that end in the year 2024:**  
   Write a query to select courses where the `endDate` is in the year 2024. Use the `YEAR()` function to extract the year from the `endDate`.

8. **Select courses with the subject 'a450' and ordered by `period`:**  
   Write a query to select courses with `subjectId` 'a450' and order them by `period` in ascending order.

9. **Count the total number of courses:**  
   Write a query to count the total number of courses in the `course` table.

10. **Select courses where `endDate` is earlier than `startDate`:**  
    Write a query to find any courses where the `endDate` is earlier than the `startDate`. Use the comparison operator (`<`).
1. **Use the `=` operator to find a specific course:**  
   Write a query to select the course with `subjectId` equal to 'a290'.

2. **Use the `!=` (not equal) operator to exclude a specific course:**  
   Write a query to select all courses where the `subjectId` is not 'a450'.

3. **Use the `LIKE` operator to find courses with a subject that starts with 'a':**  
   Write a query to find all courses where the `subjectId` starts with the letter 'a'. Use the `LIKE` operator and a wildcard.

4. **Use the `BETWEEN` operator to find courses with a `period` between 1 and 3:**  
   Write a query to find all courses where the `period` is between 1 and 3, inclusive.

5. **Use the `IN` operator to find courses in a specific set of subjects:**  
   Write a query to find all courses where the `subjectId` is either 'a290', 'a450', or 'b210'.

6. **Use the `IS NULL` operator to find courses with no teacher assigned:**  
   Write a query to find all courses where the `teacherId` is `NULL`.

7. **Use the `AND` operator to filter by multiple conditions:**  
   Write a query to select all courses where the `period` is 1 **and** the `participants` are greater than 5.

8. **Use the `OR` operator to find courses matching one of two conditions:**  
   Write a query to select courses where the `teacherId` is either 'h123' **or** the number of `participants` is greater than 10.

9. **Use the `NOT` operator to exclude specific results:**  
   Write a query to find all courses where the `teacherId` is **not** 'h123'.

10. **Use a combination of operators to find complex results:**  
    Write a query to find all courses that start after '2024-01-01' **and** have more than 8 participants, **or** have no assigned teacher (`teacherId` is NULL).