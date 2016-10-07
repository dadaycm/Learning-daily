```
.exit / .quit
.help

sqlite3 toy_app.db
.read toy.sql
.dump 

sqlite3 development.sqlite3 .dump > ~/toy.sqlite3

.schema
.dump
.read FILENAME   # execute SQL from FILENAME which is from .dump

.headers on
.mode column
SELECT * from USERS;

.mode csv
.mode insert     #(.dump)


.mode List   #(.separator STRING)
.seperator |


```
