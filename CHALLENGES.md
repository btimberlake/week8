# SQL Challenges

```
sqlite3 movies.db

sqlite3> .mode column
sqlite3> .headers on
sqlite3> .width 30 30 30 30
```

* Feel free to refer to the [Quick Reference in the README](README.md)
* Curiosity an experimentation are required

### Single-Table Queries

Write SQL code that will answer the following questions.  (Hint: You might need to enter
multiple SQL commands in order to come up with the answer.)

1. How many movies are in the database?
2. How many actors are there?
3. What are the first 10 movies in alphabetical order?
4. What are the top 10 movies based on the `vote_average` column?
5. How many movies does Tom Hanks appear in?
6. Who directed the highest-rated movie?

### Multi-Table Queries

1. Generate a report that has the following columns: title, director (the name, not the ID), and release date.
2. Who starred in Apollo 13?
3. Which movies were directed by Steven Spielberg?
4. Generate a list of directors and the number of movies they directed.
