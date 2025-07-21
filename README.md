# codes
 * Method 2 (Start Menu/Search):
   * Search for "SQL*Plus" in your Windows 8 Start screen or Apps list.
   * Click on "SQL*Plus" to open it.
3. Connect to Your Database:
Once SQL*Plus is open, you'll be prompted to enter your username and password.
SQL*Plus: Release 10.2.0.1.0 - Production on Mon Jul 21 13:19:50 2025

Copyright (c) 1982, 2005, Oracle. All rights reserved.

Enter user-name: SYSTEM  (or your database user, e.g., HR, SCOTT)
Enter password: your_password

4. Execute the SQL File using @ or START command:
Once connected, you can use the @ or START command followed by the full path to your text file.
 * Using @:
   @C:\Users\YourUsername\Desktop\my_queries.txt

 * Using START:
   START C:\Users\YourUsername\Desktop\my_queries.txt

Explanation:
 * @ (At sign) or START: These are SQLPlus commands that tell SQLPlus to read and execute the commands from the specified file.
 * Full Path: You need to provide the complete path to your text file.
Important Considerations:
 * File Extension: While .txt works, it's common practice to use .sql for SQL script files. SQL*Plus doesn't strictly care about the extension, but .sql makes it clear what the file contains.
 * Error Handling: If there are errors in your SQL file, SQL*Plus will typically display them as it processes the file.
 * SET ECHO ON (Optional but Recommended): If you want to see the commands being executed on the screen as they are processed from the file, you can add SET ECHO ON; at the beginning of your SQL file or execute it directly in SQL*Plus before running your script.
   SET ECHO ON;
@C:\Users\YourUsername\Desktop\my_queries.txt

 * COMMIT; and ROLLBACK;: If your SQL file contains DML statements (INSERT, UPDATE, DELETE), remember that they won't be permanently saved to the database until you issue a COMMIT; command. If something goes wrong and you want to undo the changes, you can use ROLLBACK;. You can include these commands within your my_queries.txt file as well.
 * SPOOL (Optional for Output): If you want to save the output of your queries to another text file, you can use the SPOOL command:
   SPOOL C:\Users\YourUsername\Desktop\query_output.txt
@C:\Users\YourUsername\Desktop\my_queries.txt
SPOOL OFF

By following these steps, you can easily execute your SQL queries from a text file on your Windows 8 desktop in your Oracle 10g environment.
