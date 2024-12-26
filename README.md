- 26.3 SQL Relationships
- Using Keys:
    - CREATE TABLE studios (id SERIAL PRIMARY KEY, name TEXT, founded_in TEXT);
- Joining Tables
    - JOIN Operation
        - Data from tables is matched according to a join condition
        - Data can compare a foreign key from one table and a primary key to another table
        - SELECT title, name FROM movies JOIN studios ON movies.studio_id = studios.id;
        - SELECT title, name FROM movies INNER JOIN studios ON movies.studio_id = studios.id;
- Types of Joins
    - Inner - Only the rows that match the condition in both tables
    - Outer
        - Left - All of the rows from the first table (left), combined with matching rows from the second table (right)
        - Right - The matching rows from the first table (right), combined with all the rows from the second table (left)
        - Full - All the rows from both tables (left and right)

- Many-to-Many Relationships - ex: (a movie is made up of many actors. Each actor is also part of many different movies)
    - SELECT * FROM movies JOIN roles ON movies.id = roles.movie_id JOIN actors ON roles.actor_id = actors.id;

______________________________________________________________
- Exercise:
    - Part 1
        - psql < data.sql
        - psql joins_exercise
    - Part 2
        - https://sqlzoo.net/wiki/SQL_Tutorial
            - 6 and 7