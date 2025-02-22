Database Creation and Data Import Process
1.Direct Import of Data:
Data was directly imported into the Shows table using a Netflix.csv file via the pgAdmin Import Data function. The file contained key information about shows, including actors, directors, categories, ratings, release years, and more.

2.create.sql:
This file contains SQL statements to define the structure of all tables, including:
Actors, Countries, Categories, and Directors.
It specifies columns, data types, primary keys, and foreign key relationships.

3.load.sql:
Data Insertion:
Data from the Shows table was split into individual rows for related entities (e.g., actors, countries, categories, directors) and inserted into their respective tables with unique identifiers (actor_id, country_id, category_id, director_id).

Relationships & Constraints:
New columns (country_id, director_id, actor_id, category_id) were added to the Shows table.
Foreign key constraints were established to link the Shows table with related tables for referential integrity.

Data Updates:
The Shows table was updated to populate the newly added foreign key columns by matching titles with the corresponding entries in related tables.

Indexes & Integrity:
Indexes were created on foreign key columns and other frequently queried columns such as release_year, rating, and type to optimize query performance.
Constraints (e.g., NOT NULL, CHECK) were applied to maintain data integrity.
This process ensured that the database is well-structured, normalized, and optimized for efficient querying and management of the Netflix data.