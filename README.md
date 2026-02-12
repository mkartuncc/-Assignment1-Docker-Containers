# What the stack does (2–3 sentences)
This stack has two parts hosted in Docker and Docker compose, with one container running a PostgreSQL database and the other running a lightweight Python application. The database starts with an intital seeded table containing trip information. The Python application then accesses the database to print statistics.  
# Exact commands to run/stop
After downloading the files present in this repository and navigating to the folder in your terminal, start the application by running either

If you have the 'make' utility downloaded: 
> make

If not:
> docker compose up --build

To stop at any time:
> Ctrl + C
# Example output screenshot 
![screenshot of JSON summary](/json_summary.png)

# Example output (copy/paste)
app-1  | === Summary ===

app-1  | {

app-1  |   "total_trips": 6,

app-1  |   "avg_fare_by_city": [

app-1  |     {

app-1  |       "city": "New York",

app-1  |       "avg_fare": 19.0

app-1  |     },

app-1  |     {

app-1  |       "city": "San Francisco",

app-1  |       "avg_fare": 20.25

app-1  |     },

app-1  |     {

app-1  |       "city": "Charlotte",

app-1  |       "avg_fare": 16.25

app-1  |     }

app-1  |   ],

app-1  |   "top_by_minutes": [

app-1  |     {

app-1  |       "city": "San Francisco",

app-1  |       "minutes": 28

app-1  |     },

app-1  |     {

app-1  |       "city": "New York",

app-1  |       "minutes": 26

app-1  |     },

app-1  |     {

app-1  |       "city": "Charlotte",

app-1  |       "minutes": 21

app-1  |     },

app-1  |     {

app-1  |       "city": "Charlotte",

app-1  |       "minutes": 12

app-1  |     },

app-1  |     {

app-1  |       "city": "San Francisco",

app-1  |       "minutes": 11

app-1  |     }

app-1  |   ]

app-1  | }

app-1 exited with code 0
# Where outputs are written
The output will appear as a JSON summary printed directly to your terminal and in the out/ folder: 
# Troubleshooting (DB not ready, permission on out/, etc.) 
DB not ready --> try restaring Docker and deleting all associated containers

permissions --> ensure that you have write permissions, or use an admin account if possible
