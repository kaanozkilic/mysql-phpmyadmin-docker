## In-Class Task 4: Working with Tables - Select & Operators

You are required to use the following database [sampleDb.sql](https://dipaish.github.io/databases/sampleDb.sql) for the tasks below:

1. **Select all records from the `course` table:**  
   Write a query to select all columns and rows from the `course` table.

   ```
   mysql> SELECT * FROM course;
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a290      |      1 | h430      |            4 | 2011-08-01 | 2011-09-15 |
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL       |
   | a450      |      1 | h303      |            2 | 2011-01-03 | 2011-02-25 |
   | a450      |      2 | h560      |            2 | 2011-12-01 | 2012-03-10 |
   | a480      |      1 | h180      |            3 | 2012-02-10 | 2012-04-22 |
   | a480      |      2 | h784      |            2 | 2012-03-15 | 2012-05-30 |
   | a730      |      1 | h290      |            6 | 2012-03-15 | 2012-05-30 |
   | a760      |      1 | h786      |            4 | 2012-06-15 | 2012-08-15 |
   +-----------+--------+-----------+--------------+------------+------------+
   8 rows in set (0.00 sec)
   ```

2. **Select courses with more than 5 participants:**  
   Write a query to retrieve courses where the number of participants is greater than 5.

   ```
   mysql> SELECT * FROM course WHERE participants > 5;
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a730      |      1 | h290      |            6 | 2012-03-15 | 2012-05-30 |
   +-----------+--------+-----------+--------------+------------+------------+
   1 row in set (0.00 sec)
   ```

3. **Select courses that have no assigned teacher:**  
   Write a query to select all courses where `teacherId` is `NULL`.

   ```
   mysql> SELECT * FROM course WHERE teacherId IS NULL; 
   +-----------+--------+-----------+--------------+------------+---------+
   | subjectId | period | teacherId | participants | startDate  | endDate |
   +-----------+--------+-----------+--------------+------------+---------+
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL    |
   +-----------+--------+-----------+--------------+------------+---------+
   1 row in set (0.00 sec)
   ```

4. **Select courses starting after '2024-01-01':**  
   Write a query to retrieve all courses where the `startDate` is after '2024-01-01'.

   ```
   mysql> SELECT * FROM course WHERE startDate > "2024-01-01"; 
   Empty set (0.00 sec)
   ```

5. **Select courses with participants between 3 and 8:**  
   Write a query to find all courses that have between 3 and 8 participants, inclusive.

   ```
   mysql> SELECT * FROM course WHERE participants >= 3 AND participants <= 8; 
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a290      |      1 | h430      |            4 | 2011-08-01 | 2011-09-15 |
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL       |
   | a480      |      1 | h180      |            3 | 2012-02-10 | 2012-04-22 |
   | a730      |      1 | h290      |            6 | 2012-03-15 | 2012-05-30 |
   | a760      |      1 | h786      |            4 | 2012-06-15 | 2012-08-15 |
   +-----------+--------+-----------+--------------+------------+------------+
   5 rows in set (0.00 sec)
   ```

6. **Select courses for a specific teacher:**  
   Write a query to retrieve all courses taught by the teacher with `teacherId` 'h123'.

   ```
   mysql> SELECT * FROM course WHERE teacherId = "h123";    
   Empty set (0.00 sec)
   ```

7. **Select courses that end in the year 2024:**  
   Write a query to select courses where the `endDate` is in the year 2024. Use the `YEAR()` function to extract the year from the `endDate`.

   ```
   mysql> SELECT * FROM course WHERE YEAR(endDate) = 2024; 
   Empty set (0.01 sec)
   ```

8. **Select courses with the subject 'a450' and ordered by `period`:**  
   Write a query to select courses with `subjectId` 'a450' and order them by `period` in ascending order.

   ```
   mysql> SELECT * FROM course WHERE subjectId = "a450" ORDER BY period ASC;
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a450      |      1 | h303      |            2 | 2011-01-03 | 2011-02-25 |
   | a450      |      2 | h560      |            2 | 2011-12-01 | 2012-03-10 |
   +-----------+--------+-----------+--------------+------------+------------+
   2 rows in set (0.00 sec)
   ```

9. **Count the total number of courses:**  
   Write a query to count the total number of courses in the `course` table.

   ```
   mysql> SELECT COUNT(*) FROM course;
   +----------+
   | COUNT(*) |
   +----------+
   |        8 |
   +----------+
   1 row in set (0.00 sec)
   ```

10. **Select courses where `endDate` is earlier than `startDate`:**  
   Write a query to find any courses where the `endDate` is earlier than the `startDate`. Use the comparison operator (`<`).

   ```
   mysql> SELECT * FROM course WHERE endDate < startDate;                    
   Empty set (0.00 sec)
   ```

1. **Use the `=` operator to find a specific course:**  
   Write a query to select the course with `subjectId` equal to 'a290'.

   ```
   mysql> SELECT * FROM course WHERE subjectId = "a290";  
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a290      |      1 | h430      |            4 | 2011-08-01 | 2011-09-15 |
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL       |
   +-----------+--------+-----------+--------------+------------+------------+
   2 rows in set (0.00 sec)
   ```

2. **Use the `!=` (not equal) operator to exclude a specific course:**  
   Write a query to select all courses where the `subjectId` is not 'a450'.

   ```
   mysql> SELECT * FROM course WHERE subjectId != "a450"; 
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a290      |      1 | h430      |            4 | 2011-08-01 | 2011-09-15 |
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL       |
   | a480      |      1 | h180      |            3 | 2012-02-10 | 2012-04-22 |
   | a480      |      2 | h784      |            2 | 2012-03-15 | 2012-05-30 |
   | a730      |      1 | h290      |            6 | 2012-03-15 | 2012-05-30 |
   | a760      |      1 | h786      |            4 | 2012-06-15 | 2012-08-15 |
   +-----------+--------+-----------+--------------+------------+------------+
   6 rows in set (0.00 sec)
   ```

3. **Use the `LIKE` operator to find courses with a subject that starts with 'a':**  
   Write a query to find all courses where the `subjectId` starts with the letter 'a'. Use the `LIKE` operator and a wildcard.

   ```
   mysql> SELECT * FROM course WHERE subjectId LIKE "a%"; 
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a290      |      1 | h430      |            4 | 2011-08-01 | 2011-09-15 |
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL       |
   | a450      |      1 | h303      |            2 | 2011-01-03 | 2011-02-25 |
   | a450      |      2 | h560      |            2 | 2011-12-01 | 2012-03-10 |
   | a480      |      1 | h180      |            3 | 2012-02-10 | 2012-04-22 |
   | a480      |      2 | h784      |            2 | 2012-03-15 | 2012-05-30 |
   | a730      |      1 | h290      |            6 | 2012-03-15 | 2012-05-30 |
   | a760      |      1 | h786      |            4 | 2012-06-15 | 2012-08-15 |
   +-----------+--------+-----------+--------------+------------+------------+
   8 rows in set (0.00 sec)
   ```

4. **Use the `BETWEEN` operator to find courses with a `period` between 1 and 3:**  
   Write a query to find all courses where the `period` is between 1 and 3, inclusive.

   ```
   mysql> SELECT * FROM course WHERE period BETWEEN 1 AND 3; 
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a290      |      1 | h430      |            4 | 2011-08-01 | 2011-09-15 |
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL       |
   | a450      |      1 | h303      |            2 | 2011-01-03 | 2011-02-25 |
   | a450      |      2 | h560      |            2 | 2011-12-01 | 2012-03-10 |
   | a480      |      1 | h180      |            3 | 2012-02-10 | 2012-04-22 |
   | a480      |      2 | h784      |            2 | 2012-03-15 | 2012-05-30 |
   | a730      |      1 | h290      |            6 | 2012-03-15 | 2012-05-30 |
   | a760      |      1 | h786      |            4 | 2012-06-15 | 2012-08-15 |
   +-----------+--------+-----------+--------------+------------+------------+
   8 rows in set (0.00 sec)
   ```

5. **Use the `IN` operator to find courses in a specific set of subjects:**  
   Write a query to find all courses where the `subjectId` is either 'a290', 'a450', or 'b210'.

   ```
   mysql> SELECT * FROM course WHERE subjectId IN ("a290", "a450", "b210"); 
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a290      |      1 | h430      |            4 | 2011-08-01 | 2011-09-15 |
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL       |
   | a450      |      1 | h303      |            2 | 2011-01-03 | 2011-02-25 |
   | a450      |      2 | h560      |            2 | 2011-12-01 | 2012-03-10 |
   +-----------+--------+-----------+--------------+------------+------------+
   4 rows in set (0.00 sec)
   ```

6. **Use the `IS NULL` operator to find courses with no teacher assigned:**  
   Write a query to find all courses where the `teacherId` is `NULL`.

   ```
   mysql> SELECT * FROM course WHERE teacherId IS NULL;     
   +-----------+--------+-----------+--------------+------------+---------+
   | subjectId | period | teacherId | participants | startDate  | endDate |
   +-----------+--------+-----------+--------------+------------+---------+
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL    |
   +-----------+--------+-----------+--------------+------------+---------+
   1 row in set (0.00 sec)
      ```

7. **Use the `AND` operator to filter by multiple conditions:**  
   Write a query to select all courses where the `period` is 1 **and** the `participants` are greater than 5.

   ```
   mysql> SELECT * FROM course WHERE period = 1 AND participants > 5; 
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a730      |      1 | h290      |            6 | 2012-03-15 | 2012-05-30 |
   +-----------+--------+-----------+--------------+------------+------------+
   1 row in set (0.00 sec)
   ```

8. **Use the `OR` operator to find courses matching one of two conditions:**  
   Write a query to select courses where the `teacherId` is either 'h123' **or** the number of `participants` is greater than 10.

   ```
   mysql> SELECT * FROM course WHERE teacherId = "h123" OR participants > 10; 
   Empty set (0.00 sec)
   ```

9. **Use the `NOT` operator to exclude specific results:**  
   Write a query to find all courses where the `teacherId` is **not** 'h123'.

   ```
   mysql> SELECT * FROM course WHERE NOT teacherId = "h123"; 
   +-----------+--------+-----------+--------------+------------+------------+
   | subjectId | period | teacherId | participants | startDate  | endDate    |
   +-----------+--------+-----------+--------------+------------+------------+
   | a290      |      1 | h430      |            4 | 2011-08-01 | 2011-09-15 |
   | a450      |      1 | h303      |            2 | 2011-01-03 | 2011-02-25 |
   | a450      |      2 | h560      |            2 | 2011-12-01 | 2012-03-10 |
   | a480      |      1 | h180      |            3 | 2012-02-10 | 2012-04-22 |
   | a480      |      2 | h784      |            2 | 2012-03-15 | 2012-05-30 |
   | a730      |      1 | h290      |            6 | 2012-03-15 | 2012-05-30 |
   | a760      |      1 | h786      |            4 | 2012-06-15 | 2012-08-15 |
   +-----------+--------+-----------+--------------+------------+------------+
   7 rows in set (0.00 sec)
   ```

10. **Use a combination of operators to find complex results:**  
   Write a query to find all courses that start after '2024-01-01' **and** have more than 8 participants, **or** have no assigned teacher (`teacherId` is NULL).

   ```
   mysql> SELECT * FROM course WHERE startDate > "2024-01-01" AND participants > 8 OR teacherId IS NULL; 
   +-----------+--------+-----------+--------------+------------+---------+
   | subjectId | period | teacherId | participants | startDate  | endDate |
   +-----------+--------+-----------+--------------+------------+---------+
   | a290      |      2 | NULL      |            5 | 2011-11-01 | NULL    |
   +-----------+--------+-----------+--------------+------------+---------+
   1 row in set (0.00 sec)
   ```
