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

Selecting all columns from a table

```sql
SELECT
*
From
crew
 ```
This query allowed me to retrieve all of the columns from the crew table.

<img width="566" height="514" alt="Screenshot 2025-12-15 at 4 25 10 PM" src="https://github.com/user-attachments/assets/ad51ea05-f67a-481f-9c14-ec3cf28a7748" />

<img width="513" height="514" alt="Screenshot 2025-12-15 at 4 25 45 PM" src="https://github.com/user-attachments/assets/3d10badb-95bc-4529-a2d3-a92d31710a6d" />


# Chapter 4 Filtering results with where

<img width="739" height="759" alt="Screenshot 2025-12-15 at 4 36 02 PM" src="https://github.com/user-attachments/assets/e8b4daa1-cfa7-4470-aa77-0de7ec4cd262" />

Get all of the columns from the "crew" table where staff_name is 'Helga Sinclair'

```sql
SELECT *
from crew
where staff_name is  'Helga Sinclair'
 ```

This query allowed me to retrieve all of the columns from the crew table where staff_name matched 'Helga Sinclair'

Filtering results with where


<img width="727" height="378" alt="Screenshot 2025-12-15 at 4 37 10 PM" src="https://github.com/user-attachments/assets/3b2e54b7-2f6a-44c3-b045-24a4b4ee5e61" />

# Chapter 5

<img width="690" height="909" alt="Screenshot 2025-12-15 at 4 42 09 PM" src="https://github.com/user-attachments/assets/aaf6eb0b-0e28-4bfa-8332-ad71cb54e00a" />


Get all of the columns from the "pods_list" table where status is 'functioning', and range is more than 1500.


/*
Select all of the escape pods where the range is over 1500 and status is 'functioning'.
*/

```sql
SELECT *
FROM pods_list 
where status is 'functioning'
and
range > 1500
 ```

This query allowed me to retrieve all of the columns from the pods_list table where status matched 'functioning' and range was greater than 1500

Using multiple where conditions

<img width="570" height="591" alt="Screenshot 2025-12-15 at 4 45 31 PM" src="https://github.com/user-attachments/assets/3d931615-c4bc-4bb4-9e3b-7546635be267" />

# Chapter 6 Using where, or, not

<img width="589" height="801" alt="Screenshot 2025-12-15 at 4 47 57 PM" src="https://github.com/user-attachments/assets/748f2dba-1320-49e1-802b-3f2863d29b71" />

You need to find all of the "circuits" where area is "pod 03", OR status is NOT "green".

/*
Select all of the circuits where the area is 'pod 03' or the status is NOT green.
*/

```sql
SELECT *
From circuits
where area is "pod 03"
or status is NOT "green"
 ```
This query allowed me to retrieve all of the columns from the circuits table where status matched not "green and area is "pod 03"

Using where, or, not

<img width="559" height="606" alt="Screenshot 2025-12-15 at 4 51 17 PM" src="https://github.com/user-attachments/assets/82e327f4-19b2-4a7e-89f4-fbc609852784" />

# Chapter 7 Grouping and counting

<img width="677" height="672" alt="Screenshot 2025-12-15 at 4 55 31 PM" src="https://github.com/user-attachments/assets/53e93e89-dc12-47f6-bd0b-9feda341fecf" />

You need to find out how many of the crew are in different places. Count the staff_name column grouped by the last_location column.

Call your new staff count column crew_count.
/*
Count the crew based on their last known location. 

(Use the staff_name column in your count - we could use any column to count but we're going to use staff_name). 

Call the column you make 'crew_count'.
*/

```sql
SELECT
    last_location,
    COUNT(staff_name) AS crew_count
FROM crew
GROUP BY last_location
 ```

<img width="662" height="659" alt="Screenshot 2025-12-15 at 5 01 39 PM" src="https://github.com/user-attachments/assets/48f3e8eb-8812-4196-a9fa-61159c1e0795" />

# Chapter 8 Multi-column grouping

<img width="687" height="724" alt="Screenshot 2025-12-15 at 5 04 12 PM" src="https://github.com/user-attachments/assets/b9453845-eaa4-4269-9730-e626b81d9f05" />

You need to find out how many of the crew are in different places, AND what different states of health. Group by the the last_location column and the status column. Count the staff_name column and call it crew_count.

```sql
SELECT
    last_location,
	status,
    COUNT(staff_name) as crew_count
FROM crew
GROUP BY last_location, status
 ```

Multi-column grouping

<img width="693" height="661" alt="Screenshot 2025-12-15 at 5 08 43 PM" src="https://github.com/user-attachments/assets/b5315a7a-623c-48f0-9a99-bdb34e1aeb57" />

# Chapter 9 Filtering and grouping

<img width="670" height="909" alt="Screenshot 2025-12-15 at 5 11 24 PM" src="https://github.com/user-attachments/assets/5445b346-b8b1-43bb-a29c-3373bf8dd4c2" />

You need to group your crew based on the pods they are heading for, to find out if any groups have a particularly high total weight, are particularly large or far away from their pod.

Group everyone by pod group but only if their status is not 'deceased', sum their weights and call it total_weight, find the max distance from the pod and call it max_distance.

/*

For all of the members of crew who are NOT DECEASED - find the total combined weight for each pod_group (call it total_weight). 

Also find the maximum distance that any of them
are from a pod (call it max_distance).
*/

```sql
SELECT pod_group,
sum (weight_kg) as total_weight,
max(distance_to_pod) as max_distance 
from crew
where status != 'deceased'
GROUP BY pod_group

```
<img width="661" height="673" alt="Screenshot 2025-12-15 at 5 21 02 PM" src="https://github.com/user-attachments/assets/11bab937-c27a-4309-a263-249cae994807" />


