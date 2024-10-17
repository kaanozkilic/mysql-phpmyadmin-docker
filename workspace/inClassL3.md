## In-Class Task 3: Working with Tables - Insert Into

You are required to use the following database [sampleDb.sql](https://dipaish.github.io/databases/sampleDb.sql) for the tasks below:

1. **Insert a new course:**  
   Insert a course with `subjectId` 'a350', `period` '1', `teacherId` 'h123', and 10 participants, starting on '2024-01-10' and ending on '2024-03-01'.

2. **Insert a course without an assigned teacher:**  
   If a course has no assigned teacher (`teacherId` is NULL), insert a course with `subjectId` 'b210', `period` '2', 8 participants, and starting on '2024-04-01'.

3. **Insert multiple courses in a single query:**  
   Insert the following courses in one `INSERT INTO` statement:  
   - `subjectId` 'c320', `period` '1', `teacherId` 'h987', with 5 participants  
   - `subjectId` 'd110', `period` '2', `teacherId` 'h654', with 7 participants.

4. **Insert a course with minimal information:**  
   Insert a course with only the `subjectId` 'b101' and `period` '3', leaving all other fields (`teacherId`, `participants`, `startDate`, `endDate`) as `NULL`.

5. **Insert a course with complete date information:**  
   Insert a course that started on '2023-09-01' and ended on '2023-10-15', with `subjectId` 'a520', `period` '2', `teacherId` 'h210', and 12 participants.

6. **Insert a course with an unknown end date:**  
   Insert a course where the start date is known ('2024-05-10') but the end date is still unknown (NULL). The course has `subjectId` 'e510', `period` '3', `teacherId` 'h789', and 6 participants.

7. **Insert a course without specifying participants:**  
   Insert a course with `subjectId` 'f320', `period` '1', `teacherId` 'h112', and starting on '2024-02-15', but without specifying the number of participants (it should default to NULL).

8. **Insert a course without start or end dates:**  
   Insert a course with `subjectId` 'g210', `period` '2', `teacherId` 'h325', and 4 participants, but leave both `startDate` and `endDate` as `NULL`.

9. **Insert a course with only the start date provided:**  
   Insert a course with `subjectId` 'h100', `period` '4', `teacherId` 'h999', with 9 participants, starting on '2024-07-01', but leaving the `endDate` as `NULL`.

10. **Insert multiple courses, one with missing fields:**  
    Insert the following two courses in one `INSERT INTO` statement:  
   - `subjectId` 'i340', `period` '1', `teacherId` 'h876', with 11 participants, starting on '2024-08-15', and ending on '2024-10-01'.  
   - `subjectId` 'j290', `period` '2', with no assigned teacher and no start or end dates.
