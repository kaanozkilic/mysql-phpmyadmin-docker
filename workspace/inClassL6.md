## In-Class Task 6: Working with Tables - Create Index & View

You are required to use the following database [sampleDb.sql](https://dipaish.github.io/databases/sampleDb.sql) for the tasks below:

### Indexes:

1. **Create an index on the `teacherId` column in the `course` table:**  
   Write a query to create an index named `idx_teacherId` on the `teacherId` column.

2. **Create a composite index on `subjectId` and `period`:**  
   Write a query to create an index named `idx_subject_period` on both `subjectId` and `period` in the `course` table.

3. **Show all indexes for the `course` table:**  
   Write a query to display all indexes created in the `course` table.

4. **Drop the index `idx_teacherId`:**  
   Write a query to drop the index `idx_teacherId` from the `course` table.

5. **Explain the purpose of creating an index on a column like `teacherId`:**  
   Discuss why creating an index on a frequently searched column, like `teacherId`, improves query performance.

### Views:

6. **Create a view to display courses with more than 5 participants:**  
   Write a query to create a view called `view_large_courses` that shows courses with more than 5 participants.

7. **Create a view showing courses and their start and end dates:**  
   Write a query to create a view called `view_course_dates` that shows `subjectId`, `startDate`, and `endDate` from the `course` table.

8. **Update the `view_course_dates` view to include the `teacherId`:**  
   Write a query using `CREATE OR REPLACE VIEW` to add the `teacherId` column to the `view_course_dates`.

9. **Retrieve data from the view `view_large_courses`:**  
   Write a query to select all data from the `view_large_courses`.

10. **Drop the view `view_course_dates`:**  
    Write a query to drop the view `view_course_dates` from the database.
