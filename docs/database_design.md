# Database Design

## people

Stores information about members of Congress.

| Column | Type | Description |
|----------|----------|----------|
| id | SERIAL | Primary Key |
| full_name | VARCHAR(200) | Person's full name |
| person_type	| VARCHAR(20) |	politician, spouse |
| related_to	| VARCHAR(200) |	Related politician (if spouse) |
| chamber | VARCHAR(20) | House, Senate, NULL |
| party | VARCHAR(20) | Democrat, Republican, Independent, NULL |
| state | VARCHAR(10) | State abbreviation |
| is_active | BOOLEAN | Active member of Congress |
| created_at | TIMESTAMP | Record creation date |
