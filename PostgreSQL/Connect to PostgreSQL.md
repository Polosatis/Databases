# Ways to connect to PostgreSQL

## Command line

Use the command line to connect to your database:

```
psql -h [ip address] -p [port] -d [database] -U [username]
```

## Python

Include the code below in your script to connect to your database and fetch teh records from it

```
import psycopg2

# Connect to your PostgreSQL database on a remote server
conn = psycopg2.connect(host="POSTGRES_IP_ADDRESS", port="5432", dbname="DATABASE_NAME", user="DB_USER", password="DB_USER_PASSWORD")

# Open a cursor to perform database operations
cur = conn.cursor()

# Execute a test query
cur.execute("SELECT * FROM mytable")

# Retrieve query results
records = cur.fetchall()

# Finally, you may print the output to the console or use it anyway you like
print(records)
```
