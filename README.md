# DatabaseAnalytics_2

Simple sql queries

CARPENTER_(1)


Download “CARPENTER.sql” from ICON, then upload into APEX and run. This
script contains 88 SQL statements to create and populate a database tracking
information about the films of John Carpenter, best known as the creator and
director of the *Halloween *movie
franchise. This data is sourced from IMDB ([https://www.imdb.com)](https://www.imdb.com) and Wikipedia ([https://en.wikipedia.org/wiki/John_Carpenter](https://en.wikipedia.org/wiki/John_Carpenter)). The normalized database contains 5 tables:

* FILM
  stores the unique ID, type (feature movie, video release, TV movie, or
  short film), title, and release year for all films where Carpenter had a
  principal role. In addition, it records the length (in minutes), average
  IMDB user rating (out of 10), total number of IMDB user votes, estimated budget
  (i.e., cost), estimated box office revenue, and production company for
  each film, though these fields may have missing values. (46 rows total)
* GENRE
  tracks the genre (e.g., Horror, Drama) of each film. Each movie is
  associated with 1-3 genres. (101 rows total)
* PERSON
  contains the unique ID, name, birth year, and death year for people that
  have worked on films with Carpenter (including John Carpenter himself).
  While all people have a first name, some people are missing the other name
  components, birth year, and/or death year. (266 rows total)
* CREW
  records the principal people involved in the cast and crew of each film
  and their job on the film (e.g., actor, director, producer). There are
  1-13 principal cast and crew members for each movie. All people in the
  database are associated with one or more films, and the same person may
  have multiple jobs on the same film (e.g., Carpenter wrote, directed, and
  composed for  *Halloween* ). For
  actors, there is also a character name. (435 rows total)
* AWARD
  contains information about major award nominations for films in the database.
  Each row records a unique award ID, film ID, award name, award category,
  and a binary (0/1) variable tracking whether it won the award. A film may
  be nominated for 0 awards, but may also be nominated for multiple awards.
  (30 rows total)

You should review each table in the Object Browser and/or examine the
SQL script to make sure that you understand the field definitions, constraints,
primary key(s), foreign key(s), and relationships. A logical relational schema
for the data is displayed below
