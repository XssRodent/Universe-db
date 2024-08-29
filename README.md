# Universe SQL

## Overview

Welcome to the Universe SQL project! This project is part of the FreeCodeCamp "Build a Celestial Bodies Database" challenge. The goal of this project is to create a PostgreSQL database that models various celestial bodies in our universe, including planets, stars, and other objects.

## Project Structure

The `universe.sql` file contains SQL statements for:

- **Creating Tables:** Defines the structure of the database, including tables for planets, stars, and their relationships.
- **Inserting Data:** Populates the database with sample data for testing and demonstration purposes.
- **Queries:** Includes example queries to demonstrate how to interact with the database and retrieve information.

## Table Definitions

1. **Planets**
   - `planet_id` (INT, Primary Key)
   - `name` (VARCHAR, Name of the planet)
   - `no_of_moons` (INT, Number of moons orbiting the planet)
   - `has_water` (BOOLEAN, Indicates if the planet has water)
   - `star_id` (INT, Foreign Key, References `stars` table)

2. **Stars**
   - `star_id` (INT, Primary Key)
   - `name` (VARCHAR, Name of the star)
   - `type` (VARCHAR, Type of the star, e.g., Red Dwarf, White Dwarf)

3. **Other Tables** (If applicable)
   - Description of any additional tables included in the project.

## Getting Started

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/universe-sql.git
   cd universe-sql
Set Up the Database

Create a PostgreSQL database and run the universe.sql script to set up the schema and populate the tables.

bash
Copy code
psql -U yourusername -d yourdatabase -f universe.sql
Run Queries

Use a PostgreSQL client or command-line tool to interact with your database. Here are some example queries:

sql
Copy code
-- List all planets with their stars
SELECT planets.name AS planet_name, stars.name AS star_name
FROM planets
JOIN stars ON planets.star_id = stars.star_id;

-- Find planets with water
SELECT name FROM planets WHERE has_water = TRUE;
License
This project is licensed under the MIT License. See the LICENSE file for more details.

Acknowledgments
This project was developed as part of the FreeCodeCamp curriculum. Special thanks to the FreeCodeCamp team for their comprehensive tutorials and support.

