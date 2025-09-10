## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```
**Question 1**

  <img width="1185" height="724" alt="Screenshot 2025-09-10 132504" src="https://github.com/user-attachments/assets/3df0a1f0-b250-4497-a596-80d488c01975" />


  
**Output**:

<img width="1181" height="328" alt="Screenshot 2025-09-10 132515" src="https://github.com/user-attachments/assets/2f21ebe4-239d-4846-b805-21ff9eb00bf9" />



**Question 2**




<img width="731" height="487" alt="Screenshot 2025-09-10 132906" src="https://github.com/user-attachments/assets/5244bde6-b1ee-4010-83ef-e1a52ef7a2cb" />




**Output:**




<img width="1191" height="288" alt="Screenshot 2025-09-10 132914" src="https://github.com/user-attachments/assets/8664870a-e1d1-4a3a-a9ba-11fa3e096df6" />




**Question 3**




<img width="1200" height="588" alt="Screenshot 2025-09-10 133033" src="https://github.com/user-attachments/assets/a3d1b8b2-76ce-4747-89cf-12929c05733a" />



**Output:**



<img width="1206" height="318" alt="Screenshot 2025-09-10 133041" src="https://github.com/user-attachments/assets/c8b91103-662d-4bd3-9541-a248a987f54f" />





**Question 4**





<img width="1203" height="702" alt="Screenshot 2025-09-10 133230" src="https://github.com/user-attachments/assets/eb2fba9b-55b3-42c5-8503-b7404a418b8f" />




**Output:**




<img width="1207" height="370" alt="Screenshot 2025-09-10 133236" src="https://github.com/user-attachments/assets/fda534f4-fbe5-42da-9c04-d894ce1e8077" />



**Question 5**




<img width="1175" height="408" alt="Screenshot 2025-09-10 133322" src="https://github.com/user-attachments/assets/a5d41da1-52f8-43f5-adba-f93be615c8d4" />





**Output:**






<img width="1203" height="255" alt="Screenshot 2025-09-10 133328" src="https://github.com/user-attachments/assets/0ba0ec1f-0366-48c3-82df-bc35500b7c89" />





**Question 6**




<img width="1024" height="686" alt="Screenshot 2025-09-10 133421" src="https://github.com/user-attachments/assets/944b2595-9a7f-4065-8380-c47959c319f9" />





**Output:**






<img width="1187" height="339" alt="Screenshot 2025-09-10 133427" src="https://github.com/user-attachments/assets/990cafd9-87b7-4953-b366-c531a31742b6" />







**Question 7**





<img width="1186" height="659" alt="Screenshot 2025-09-10 133501" src="https://github.com/user-attachments/assets/aa5bb0bf-082a-4d6a-a3f2-45264eecf7a2" />





**Output:**





<img width="1206" height="297" alt="Screenshot 2025-09-10 133508" src="https://github.com/user-attachments/assets/60f62a50-46b9-4c9b-baf3-747875270949" />







**Question 8**






<img width="1174" height="700" alt="Screenshot 2025-09-10 133534" src="https://github.com/user-attachments/assets/cc6e5b56-8909-48aa-bcd3-4875d42ee67a" />





**Output:**

<img width="1204" height="337" alt="Screenshot 2025-09-10 133545" src="https://github.com/user-attachments/assets/e919c20a-8822-48ce-a58b-78020e0c430d" />





**Question 9**





<img width="1036" height="574" alt="Screenshot 2025-09-10 133605" src="https://github.com/user-attachments/assets/38e0ab0e-013c-41db-976e-33855babe6e2" />






**Output:**





<img width="1189" height="376" alt="Screenshot 2025-09-10 133610" src="https://github.com/user-attachments/assets/66ecc984-6e3f-4c04-94df-42302c9501f5" />






**Question 10**





<img width="1168" height="657" alt="Screenshot 2025-09-10 133632" src="https://github.com/user-attachments/assets/d23fc967-87a6-4d3f-8346-7c350a1b5a70" />






**Output:**






<img width="1271" height="299" alt="Screenshot 2025-09-10 133639" src="https://github.com/user-attachments/assets/e8b59ed0-49a2-44d2-9b5e-6ea6ef5405d2" />





## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
