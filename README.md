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

# Chapter 10 Sorting

<img width="658" height="677" alt="Screenshot 2025-12-15 at 6 04 04 PM" src="https://github.com/user-attachments/assets/e0f4a8bf-78f4-4566-a1f3-8de3a97cc493" />

You need to see if any of the crew are down as suspiciously light. Select the name and weight for your crew, and order the list by weight from low to high.

/*

Select the name and weight from the crew table, ordered by weight from low to high.
*/

```sql
SELECT
    staff_name,
    weight_kg
FROM crew
ORDER BY weight_kg  ASC
```

This selects the staff name and weight in kg from the crew table and orders it from low to high by weight in kg

<img width="672" height="637" alt="Screenshot 2025-12-15 at 6 13 56 PM" src="https://github.com/user-attachments/assets/3ab86697-f1b9-4987-b0dc-e3c6639a654b" />

# Chapter 11 Changing data with case statements

<img width="680" height="916" alt="Screenshot 2025-12-15 at 6 15 27 PM" src="https://github.com/user-attachments/assets/93291ca0-ad4d-4739-b7dc-9b23ce08683c" />

You need to fix the weights for the crew members that are down wrong. Select the name and weight for your crew, and create a new column called fixed_weight.

When the current weight column is over 10, then fixed_weight should match it exactly. But if it is less than 10 then the fixed_weight column should show the weight number multiplied by 10.

Order your results by weight from low-to-high to double-check that your fixed_weight column is working as you'd expect.

/*

Get the name and weight of the crew, and create a new column called fixed_weight. 

When the weight is less than 10 - multiply it by 10 in the fixed_weight column.

Order your results from low to high.

*/

```sql
SELECT 
staff_name, 
weight_kg, 
CASE 
WHEN weight_kg > 10 THEN weight_kg 
ELSE weight_kg * 10 
END AS fixed_weight 
FROM crew 
ORDER BY weight_kg
```

This selects staff name and weight in kg, then uses case to modify the columns. When the weight is greater than 10 then the weight stays the same. If not greater than 10 then it multiplies it by 10 and names the column fixed weight. Takes the data from the crew table and orders it by weight.

<img width="652" height="673" alt="Screenshot 2025-12-15 at 6 26 24 PM" src="https://github.com/user-attachments/assets/380f92e4-96aa-49d6-9baa-f0cdbf8300e8" />

# Chapter 12

<img width="674" height="824" alt="Screenshot 2025-12-15 at 6 28 09 PM" src="https://github.com/user-attachments/assets/63f438b4-afbf-4d26-b40d-230032935143" />

You need to add together all the steps from the last few levels

Filtering to only crewmates that aren't deceased
Correcting weights
Grouping by pod group and summing weights
Filtering groups to use the ones where the total weight is more than 1000 and ordering by total weight from high to low

Step 1 

/*
      Get the name, pod group, and weights for everyone in the crew table where their status is not 'deceased'
      */
	  
```sql	  
SELECT staff_name,
pod_group,
weight_kg
from crew 
where status != 'deceased'
```

Step 2

/*
Using the filtered_crew table - select the staff name and pod group. 

Create a fixed_weight column which matches the weight column if the weight is over 10, otherwise multiply the weight by 10
 */
 
 ```sql
SELECT
  staff_name,
  pod_group,
  CASE
    WHEN weight_kg > 10 THEN weight_kg
    ELSE weight_kg * 10
  END AS fixed_weight
from
  filtered_crew
```

Step 3

/*
Group the fixed_crew table based on the pod group.
Sum the fixed weight column and call it total_weight.
 */

  ```sql
SELECT
    pod_group,
    SUM(fixed_weight) AS total_weight
FROM fixed_crew
GROUP BY pod_group
```

Step 4

/*
      
Filter your grouped table to just groups where the total weight is more than 1000. 

Order by total weight from high to low.
      */

  ```sql	  
SELECT
    pod_group,
    SUM(fixed_weight) AS total_weight
FROM fixed_crew
GROUP BY pod_group
HAVING SUM(fixed_weight) > 1000
ORDER BY total_weight DESC
```

Full query 

  ```sql	
-- Filtering crew to just those who aren't 'deceased'
-----------------------------
With
  filtered_crew as (
    /*
    Get the name, pod group, and weights for everyone in the crew table where their status is not 'deceased'
     */
    SELECT
      staff_name,
      pod_group,
      weight_kg
    from
      crew
    where
      status != 'deceased'
  )
  -- End filtered_crew
  --=========================
  -- Fixing the crew weight
  -----------------------------
,
  fixed_crew as (
    /*
    Using the filtered_crew table - select the staff name and pod group. 
    
    Create a fixed_weight column which matches the weight column if the weight is over 10, otherwise multiply the weight by 10
     */
  SELECT
      staff_name,
      pod_group,
      CASE
        WHEN weight_kg > 10 THEN weight_kg
        ELSE weight_kg * 10
      END AS fixed_weight
    from
      filtered_crew
  )
  -- End fixed_crew
  --=========================
  -- Grouping the crew based on pod_group and filtering to just those groups over the threshold
  -----------------------------
,
  grouped_crew as (
    /*
    Group the fixed_crew table based on the pod group.
    Sum the fixed weight column and call it total_weight.
     */
    SELECT
      pod_group,
      SUM(fixed_weight) AS total_weight
    FROM
      fixed_crew
	     GROUP BY
      pod_group
  )
  -- End grouped_crew
  --=========================
  -- Filtering the groups to everything over 1000 and sorting from high to low
  -----------------------------
  /*
  
  Filter your grouped table to just groups where the total weight is more than 1000. 
  
  Orrder by total weight from high to low.
   */
SELECT
  pod_group,
  SUM(fixed_weight) AS total_weight
FROM
  fixed_crew
GROUP BY
  pod_group
  HAVING
  SUM(fixed_weight) > 1000
ORDER BY
  total_weight DESC
```

<img width="846" height="759" alt="Screenshot 2025-12-15 at 6 44 13 PM" src="https://github.com/user-attachments/assets/b2f02689-ff98-45da-8567-48d8595966f3" />

# Chapter 13 joining tables

<img width="672" height="793" alt="Screenshot 2025-12-15 at 6 46 48 PM" src="https://github.com/user-attachments/assets/b238bce4-d4b3-4c10-93ff-71d716feffc1" />

  Get a list of all the staff names where the party_status is not 'boarded'.

You will need to use 'join' to combine the staff names from the crew table and the party status from the evacuation_groups table.

	/*
    
Join together the crew table and evacuation_groups table based on the pod_group.

Filter to just the statuses which are not 'boarded'

Take just the staff name and party status from the result

	 */
	 
```sql	
SELECT
staff_name,
party_status
FROM crew
JOIN evacuation_groups
ON crew.pod_group = evacuation_groups.pod_group
WHERE NOT party_status = 'boarded'
```
<img width="667" height="743" alt="Screenshot 2025-12-15 at 6 53 51 PM" src="https://github.com/user-attachments/assets/526f6403-8b31-4dc8-a5e4-c17f3cd02e1c" />

# Chapter 14 Left joining tables

<img width="662" height="646" alt="Screenshot 2025-12-15 at 6 55 17 PM" src="https://github.com/user-attachments/assets/b9d184dd-258b-448d-a74a-b4d2884374d1" />

Get a list of all the staff who are in the original_crew table who aren't in the crew table.

/*
    
Get all of the crew who are in the original crew list but aren't in the current crew list.

You'll need to join and then filter based on null.

 */

```sql	
	WITH joined_crew AS (
    SELECT *
    FROM original_crew
    LEFT JOIN crew on crew.staff_id = original_crew.staff_id
)
SELECT *
FROM joined_crew
WHERE last_location IS NULL;
```

<img width="667" height="750" alt="Screenshot 2025-12-15 at 7 04 44 PM" src="https://github.com/user-attachments/assets/c0c51039-d8ea-4c40-a2b8-0f3c761ad673" />

# Chapter 15

<img width="671" height="753" alt="Screenshot 2025-12-15 at 7 32 34 PM" src="https://github.com/user-attachments/assets/18cbb494-3dd8-4bc0-97d1-c804f0472cc0" />

Get a list of all the staff in the full_crew list who don't have a current_location and whose role history doesn't end with 'Transfer' and doesn't contain 'Injured'.

Step 1 

/*
    
Group the staffing_changes table, group by the staff_name column, and combine all the rows in the role column, naming it combined_roles

  */

```sql	

SELECT
staff_name,
GROUP_CONCAT(role) as combined_roles
FROM staffing_changes
GROUP BY staff_name;
```

Step 2

/*
      
Join the grouped_changes with our full list of staff on the ship, on the staff_name column
   */
   
```sql
SELECT *
FROM full_crew
FULL OUTER JOIN grouped_changes
ON full_crew.staff_name = grouped_changes.staff_name;
```

Step 3

/*
    Filter the joined_crew to only rows where the last_location is null and the combined_roles column doesn't end with the word 'Transfer' and doesn't include the word 'Injured'
  */
	
	
```sql	
SELECT *
FROM joined_crew
WHERE last_location IS NULL
AND NOT combined_roles like '%Transfer'
AND NOT combined_roles like '%Injured%';
```

Final step 

/*
    
Get all of the crew members where there isn't a last_location, AND the most recent role change is not 'Transfer'. 

Also exclude staff whose staff record includes 'Injured'.

 */
```sql	
	WITH grouped_changes AS (
    SELECT
        staff_name,
        GROUP_CONCAT (role) as combined_roles
    FROM staffing_changes
    GROUP BY staff_name
), joined_crew AS (
    SELECT *
    FROM    full_crew
    FULL OUTER JOIN grouped_changes
ON full_crew.staff_name = grouped_changes.staff_name
)
SELECT *
FROM joined_crew
WHERE last_location IS NULL
AND NOT combined_roles like '%Transfer'
AND NOT combined_roles like '%Injured%';
```	

<img width="659" height="680" alt="Screenshot 2025-12-15 at 7 38 57 PM" src="https://github.com/user-attachments/assets/1743bb2a-801f-4efb-82e9-a98498217ff1" />

# Chapter 16

<img width="693" height="904" alt="Screenshot 2025-12-15 at 7 40 11 PM" src="https://github.com/user-attachments/assets/c3a12bbb-eb7d-4d9f-aa70-ab8922b848b5" />

Get a list of all the staff in the joined_crew list who don't have a last_location and whose role history doesn't end with 'Transfer'.

Also, exclude anyone whose role history contains 'Injured' but only if that role history doesn't include 'Returned' afterwards.

/*
    
Get all of the crew members where there isn't a last_location, AND the most recent role change is not 'Transfer'. 

ALSO EXCLUDE staff whose staff record includes 'Injured' but only if 'Injured' isn't followed by 'Returned'.

 */
	
```sql	
SELECT *
FROM joined_crew
WHERE last_location IS NULL
AND NOT combined_roles like '%Transfer'
AND (
(NOT combined_roles like '%Injured%')
        OR combined_roles like '%Injured%Returned%'
    )
```

<img width="683" height="648" alt="Screenshot 2025-12-15 at 7 42 09 PM" src="https://github.com/user-attachments/assets/42de50a7-f729-4310-a1d5-3976195c5f3b" />

# Chapter 17 Window functions

<img width="685" height="740" alt="Screenshot 2025-12-15 at 7 42 57 PM" src="https://github.com/user-attachments/assets/5c783fe1-1770-4cdf-8270-e49d294c932e" />

You have a list of times people visited each of the explosives depots - you need to find the last time a person visited each store. In your result include the following columns; staff_name, staff_id, depot, timestamp.


Step 1

/*
    
 Get everything from the depot_records table. 
      
Also create a column called reverse_ordered which uses row_number to number rows based on whether a record is the most recent time someone took something from a depot.
    
 For example, the last withdrawal from each depot should be 1, the second last should be 2.
  
  */
  
```sql		
SELECT
  *,
  ROW_NUMBER() OVER (
    PARTITION BY
      depot
    ORDER BY
      timestamp DESC
  ) as reverse_ordered
from
  depot_records
```

Step 2 

/*
      
    Get just the staff_name, staff_id, depot, and timestamp from the found_last table, but only where reverse_ordered is 1
  
 */
	
```sql	
SELECT
staff_name,
staff_id,
depot,
timestamp
FROM found_last
WHERE reverse_ordered = 1
```

Final step

/*
    
  Return a table including the columns staff_name, staff_id, depot, timestamp.

  The table should be filtered to just the last time someone took something from EACH DEPOT.

  Look at the stages for a way to figure that out.
  
*/

```sql	
	WITH found_last AS (
    SELECT
*,
        ROW_NUMBER() OVER (
                PARTITION BY depot
                ORDER BY timestamp DESC
        ) AS reverse_ordered
    FROM depot_records
)
SELECT
staff_name,
staff_id,
depot,
timestamp
FROM found_last
WHERE reverse_ordered = 1;
```

<img width="527" height="690" alt="Screenshot 2025-12-15 at 7 48 52 PM" src="https://github.com/user-attachments/assets/e2c203a9-6d26-41cb-a1b7-e6257c038705" />

Chapter 18 Column difference

<img width="548" height="860" alt="Screenshot 2025-12-15 at 7 50 29 PM" src="https://github.com/user-attachments/assets/4e95d758-2411-45ec-b54c-5ffc367315b2" />

<img width="542" height="563" alt="Screenshot 2025-12-15 at 7 50 50 PM" src="https://github.com/user-attachments/assets/2e839cc2-de60-451b-af26-904f2b423ea6" />

You have a list of call logs. Figure out which number called your spy and one other ID on the crew. Exclude any calls where the max call duration was 1.

/*
    
  Find the staff_name which is the ONLY PERSON who called one specific number that has been calling mm833, where those phone calls to mm833 lasted longer than a second
  
*/

```sql
	WITH date_to_seconds AS (
    SELECT
*,
        strftime('%s', start_time) AS start_seconds,
        strftime('%s', end_time) AS end_seconds
    FROM phone_logs
), calculated_duration AS (
    SELECT
        *,
        end_seconds - start_seconds AS duration
    FROM date_to_seconds
), suspect_numbers AS (
    SELECT phone_number
    FROM    calculated_duration
    WHERE incoming_outgoing = 'Incoming'
        AND staff_id = 'mm833'
        AND duration > 1
), suspect_individuals AS (
    SELECT *
    FROM phone_logs
    WHERE phone_number IN suspect_numbers
	        AND staff_id IS NOT 'mm833'
), distinct_calls AS (
    SELECT DISTINCT
        staff_name,
        phone_number
      FROM suspect_individuals
), counted_staff as (
    SELECT
        *,
        COUNT(staff_name) OVER (
                PARTITION BY phone_number
        ) AS staff_count
    FROM distinct_calls
)
SELECT staff_name
FROM counted_staff
WHERE staff_count = 1;
```

<img width="559" height="732" alt="Screenshot 2025-12-15 at 7 57 39 PM" src="https://github.com/user-attachments/assets/b18acf5b-fecb-4e24-b128-64e2b613a6f5" />

# Chapter 19 Concatenate Tables

<img width="541" height="907" alt="Screenshot 2025-12-15 at 8 00 20 PM" src="https://github.com/user-attachments/assets/90c16b69-0593-4a47-86d3-9f203d0d935e" />

Find all of the lifts which are below deck 2, which don't have short circuits and flooding at the same time, and don't have a loss of oxygen or broken drive shaft.

In your result, include the columns lift_name, deck, and noisy where noisy is 1 for lifts with lubricant leak and 0 for lifts without.

/*
    
  Find the lifts which have finished up on Level 1 or Level 0, which are NOT unusable (see hints for what makes a lift unusable).

  Return the columns lift_name, deck, and 'noisy' where noisy is 1 if the malfunctions will mean the lift makes lots of noise.
  
 */

 ```sql
	
With
  cleaned_lift_locations_2 as (
    SELECT
      Timestamp,
      lift_name,
      REPLACE (Location, 'Deck ', '') as Location
    FROM
      lift_locations_2
  )
  -- End cleaned_lift_locations_2
  --=========================
  -- Combining both lift location tables into one
  -----------------------------
,
  combined_locations as (
    SELECT
      time,
      lift_name,
      deck
    FROM
      lift_locations
    UNION
    SELECT
      Timestamp,
      lift_name,
      Location
    FROM
      cleaned_lift_locations_2
  )
  -- End combined_locations
  --=========================
  -- Finding the latest locations for each lift
  -----------------------------
,
  found_latest_location as (
    SELECT
      *,
      ROW_NUMBER() OVER (
        PARTITION BY
          lift_name
        ORDER BY
          time DESC
      ) as recency
    FROM
      combined_locations
  )
  -- End found_latest_location
  --=========================
  -- Filtering to just the most recent location for each lift
  -----------------------------
,
  cleaned_lift_list as (
    SELECT
      lift_name,
      deck
    FROM
      found_latest_location
    WHERE
      recency = 1
  )
  -- End cleaned_lift_list
  --=========================
  -- Categorise malfunctions as life threatening or not and noisy or not
  -----------------------------
,
  categorised_issues as (
    SELECT
      lift_name,
      malfunction,
      case
        when malfunction = 'Flooded'
        or malfunction = 'Short circuit' then 1
        else 0
      end as risk_of_electrocution,
      case
        when malfunction = 'Broken drive shaft'
        or malfunction = 'Loss of oxygen' then 1
        else 0
      end as inoperable,
      case
        when malfunction = 'Lubricant leak' then 1
        else 0
      end as noisy
    FROM
      lift_malfunctions
  )
  -- End categorised_issues
  --=========================
  -- Find just the lifts that are usable based on combinations of malfunctions
  -----------------------------
,
  usable_lifts as (
    SELECT
      lift_name,
      max(noisy) as noisy
    FROM
      categorised_issues
    GROUP BY
      lift_name
    HAVING
      sum(risk_of_electrocution) < 2
      and sum(inoperable) = 0
  )
  -- End usable_lifts
  --=========================
  -- Join together the locations and malfunctions tables and filter
  -----------------------------
SELECT
  cleaned_lift_list.lift_name,
  cleaned_lift_list.deck,
  usable_lifts.noisy
FROM
  cleaned_lift_list
  JOIN usable_lifts on cleaned_lift_list.lift_name = usable_lifts.lift_name
WHERE
  CAST(deck as FLOAT) < 2

 ```

# Chapter 20

<img width="533" height="859" alt="Screenshot 2025-12-15 at 8 15 25 PM" src="https://github.com/user-attachments/assets/edc3d206-0cbb-4020-94e2-375ff2a6da0b" />

<img width="538" height="907" alt="Screenshot 2025-12-15 at 8 15 39 PM" src="https://github.com/user-attachments/assets/e328fdf6-ce57-482b-9bb6-e25050725bc7" />

Make your choice - either look at what's in the table "readings" or delete everything after 4 June. This level will behave a little differently - see hints for more.

/*
    
  Delete every row in the readings table where the timestamp is later than 1962-06-04

  Be careful, when you're writing out the date it should be of that format (yyyy-mm-dd)
  
 */

 ```sql
SELECT *
FROM readings
WHERE timestamp >= '1962-06-04';
 ```

 ```sql
DELETE FROM readings
WHERE timestamp >= '1962-06-04'
 ```
<img width="551" height="524" alt="Screenshot 2025-12-15 at 8 20 47 PM" src="https://github.com/user-attachments/assets/445b3795-7713-40b0-981e-db4de83b1c95" />

<img width="535" height="857" alt="Screenshot 2025-12-15 at 8 21 38 PM" src="https://github.com/user-attachments/assets/2f0f9e70-26bc-4302-85fe-62a1a9ab1c6d" />



 
# Thank You

Thank you for your interest and time. Feel free to give your valuable suggestions and connect with me on [LinkedIn](https://www.linkedin.com/in/tristan-tudorof/)
