# sybase
Sybase scripts

## System Procedures

### sp_depends
Displays information about database object dependencies. you can use with the name of table and column

```sql
sp_depends table_example
```

| object         | type             |
|----------------|------------------|
| dbo.sp_example | stored procedure |

| Column         | Type  | Object Names or Column Names        |
|----------------|-------|-------------------------------------|
| column_example | index | table_example_index(column_example) |

With specific table name and column name

```sql
sp_depends table_example, column_example
```

| object         | type             |
|----------------|------------------|
| dbo.sp_example | stored procedure |

| Column         | Type  | Object Names or Column Names        |
|----------------|-------|-------------------------------------|
| column_example | index | table_example_index(column_example) |

### sp_helpgroup
Reports information about a particular group or about all groups in the current database.

| Group_name | Group_id |
|------------|----------|
| public     | 0        |

With specific group name

```sql
sp_helpgroup 'public'
```

| Group_name | Group_id | Users_in_group | Userid |
|------------|----------|----------------|--------|
| public     | 0        | dbo            | 1      |

### sp_helprotect
Reports on permissions for database objects, users, groups, or roles. you can use with username

| grantor | grantee      | type  | action           | object        | column | predicate | grantable |
|---------|--------------|-------|------------------|---------------|--------|-----------|-----------|
| dbo     | user_example | Grant | Select           | table_example | All    | NULL      | FALSE     |
| dbo     | user_example | Grant | Insert           | table_example | All    | NULL      | FALSE     |
| dbo     | user_example | Grant | Update           | table_example | All    | NULL      | FALSE     |
| dbo     | user_example | Grant | Delete           | table_example | All    | NULL      | FALSE     |
| dbo     | user_example | Grant | Execute          | sp_example    | All    | NULL      | FALSE     |
| dbo     | dbo          | Grant | Create Function  |               | All    | NULL      | FALSE     |
| dbo     | dbo          | Grant | Create Procedure |               | All    | NULL      | FALSE     |
| dbo     | dbo          | Grant | Create Table     |               | All    | NULL      | FALSE     |
| dbo     | dbo          | Grant | Create View      |               | All    | NULL      | FALSE     |

With specific username
```sql
sp_helprotect user_example
```

| grantor | grantee      | type  | action           | object        | column | predicate | grantable |
|---------|--------------|-------|------------------|---------------|--------|-----------|-----------|
| dbo     | user_example | Grant | Select           | table_example | All    | NULL      | FALSE     |
| dbo     | user_example | Grant | Insert           | table_example | All    | NULL      | FALSE     |
| dbo     | user_example | Grant | Update           | table_example | All    | NULL      | FALSE     |
| dbo     | user_example | Grant | Delete           | table_example | All    | NULL      | FALSE     |
| dbo     | user_example | Grant | Execute          | sp_example    | All    | NULL      | FALSE     |

### sp_helpuser
Displays information about all users in the current database. you can use with username

| Users_name | ID_in_db | Group_name | Login_name |
|------------|----------|------------|------------|
| dbo        | 1        | public     | sa         |

With specific username

```sql
sp_helpuser user_example
```

| Users_name   | ID_in_db | Group_name    | Login_name   |
|--------------|----------|---------------|--------------|
| user_example | 2        | group_example | user_example |
