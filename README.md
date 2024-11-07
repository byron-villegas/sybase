# sybase
Sybase scripts

## System Procedures

### sp_helpgroup
Reports information about a particular group or about all groups in the current database.

| Group_name | Group_id |
|------------|----------|
| public     | 0        |

With specific group name

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

### sp_helpuser
Displays information about all users in the current database. you can use with username

| Users_name | ID_in_db | Group_name | Login_name |
|------------|----------|------------|------------|
| dbo        | 1        | public     | sa         |
