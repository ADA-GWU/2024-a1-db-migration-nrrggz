[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/JwSLLxUh)


## *A1-DB-Migration*

- To execute the database migration outlined in the problem statement, adhere to the following instructions:

## Guidelines

1. Backing up database. It's imperative to create a backup before proceeding with any modifications to ensure we can revert to the prior state in case of any unforeseen issues.

2. Adjusting the STUDENTS table:
a. Rename the column ST_ID to STUDENT_ID.
b. Alter the data type of columns ST_NAME and ST_LAST to VARCHAR(30).

3. Updating the INTERESTS table:
a. Rename the column INTEREST to INTERESTS.
b. Modify the data type of INTERESTS to an array of strings.
c. Migrate the data stored in the INTERESTS column to conform to the new format.

4. Rollback Procedure:
Creating a script that can reverse the changes enacted during the migration process.

## Steps
1. Restoring the original state of the STUDENTS table:
a. Revert the column STUDENT_ID back to ST_ID.
b. Return the data type of columns ST_NAME and ST_LAST to VARCHAR(20).

2. Reverting changes made to the INTERESTS table:
a. Rename the column INTERESTS back to INTEREST.
b. Restore the data type of INTEREST to VARCHAR(20).
c. Convert the array format back to individual rows.

Validate the rollback:
Ensure that all tables and data have been successfully reinstated to their initial configurations.

## Additional Considerations & Conclusion:

Prior to implementing the migration in a live environment, thoroughly test both the migration and rollback procedures in a development or staging environment. We should consider documenting any modifications made during the migration process for future reference. Following these instructions will facilitate a seamless migration process, coupled with the ability to revert changes if necessary.