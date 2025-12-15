# Lost-At-SQL
In "Lost at SQL", you assume the role of a captain trapped in a sinking submarine who must use a computer terminal to navigate a vast database of information and fix the vessel. The game is broken down into chapters, each presenting specific tasks and sub-tasks that require you to write SQL queries. 

# Chapter 1

<img width="504" height="586" alt="Screenshot 2025-12-15 at 4 03 50 PM" src="https://github.com/user-attachments/assets/61e052ef-d1a6-4294-92b1-b3de9762a37c" />

Start by getting all the issues from the table "malfunctions"

```sql
SELECT
    issues
FROM
    malfunctions;
```

This query allowed me to retrieve all issues from the malfunctions table.


<img width="573" height="362" alt="Screenshot 2025-12-15 at 4 07 44 PM" src="https://github.com/user-attachments/assets/130da361-207f-417d-8641-be33a4c2cd0f" />


<img width="489" height="508" alt="Screenshot 2025-12-15 at 4 13 58 PM" src="https://github.com/user-attachments/assets/033ab8dc-37d9-4c04-9434-2f9034af7b2e" />



# Chapter 2 

<img width="731" height="588" alt="Screenshot 2025-12-15 at 4 16 41 PM" src="https://github.com/user-attachments/assets/977c0e99-6108-4223-abd6-bb108b49fabf" />

Using the "malfunctions" table again - get the issues and fix columns

```sql
SELECT
issues, fix
From
 malfunctions
 ```
This query allowed me to retrieve both the issues and the fix columns from the malfunctions table.

<img width="564" height="531" alt="Screenshot 2025-12-15 at 4 18 45 PM" src="https://github.com/user-attachments/assets/55ee3e4d-614b-4bfe-a1d4-da39f7735aae" />

<img width="545" height="507" alt="Screenshot 2025-12-15 at 4 22 51 PM" src="https://github.com/user-attachments/assets/b79833ad-8a42-410d-a4fe-f9545f93f869" />


# Chapter 3

<img width="982" height="620" alt="Screenshot 2025-12-15 at 4 24 41 PM" src="https://github.com/user-attachments/assets/9d3365d9-ab65-48e1-afb6-e422113b8ea2" />


```sql
SELECT
*
From
crew
 ```


<img width="566" height="514" alt="Screenshot 2025-12-15 at 4 25 10 PM" src="https://github.com/user-attachments/assets/ad51ea05-f67a-481f-9c14-ec3cf28a7748" />

<img width="513" height="514" alt="Screenshot 2025-12-15 at 4 25 45 PM" src="https://github.com/user-attachments/assets/3d10badb-95bc-4529-a2d3-a92d31710a6d" />




