# Introduction

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. 
The analytics team is particularly interested in understanding what songs users are listening to. 
As a data engineer 
- we have to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app and 
- then to create a Postgres database with tables designed to optimize queries on song play analysis.\
 
To do this , I have to create 

- Database schema 
- ETL pipeline for this analysis

# Database Schema

Using the song and log datasets, star schema needs to created to optimized for queries on song play analysis. This includes the following tables.

## Fact Table
1. songplays - records in log data associated with song plays i.e. records with page NextSong
   songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
## Dimension Tables
1. users - users in the app
   user_id, first_name, last_name, gender, level
2. songs - songs in music database
   song_id, title, artist_id, year, duration
3. artists - artists in music database
   artist_id, name, location, latitude, longitude
4. time - timestamps of records in songplays broken down into specific units
   start_time, hour, day, week, month, year, weekday
