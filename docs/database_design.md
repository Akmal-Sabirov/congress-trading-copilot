# Database Design

## politicians

Stores information about members of Congress.

| Column | Type | Description |
|----------|----------|----------|
| id | SERIAL | Primary Key |
| first_name | VARCHAR(100) | First Name |
| last_name | VARCHAR(100) | Last Name |
| full_name | VARCHAR(200) | Full Name |
| chamber | VARCHAR(20) | House or Senate |
| party | VARCHAR(20) | Democrat, Republican, Independent |
| state | VARCHAR(10) | State |
| is_active | BOOLEAN | Currently serving |
| created_at | TIMESTAMP | Record creation date |
