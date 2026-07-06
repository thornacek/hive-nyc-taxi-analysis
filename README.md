# NYC Taxi Big-Data Analysis with Apache Hive

_Graded practical — Johns Hopkins Big Data Analytics certificate._

**One line:** Stood up Apache Hive 4.0 in Docker and ran a suite of analytical HiveQL queries over NYC Yellow Taxi trip data — fares, tips, tolls, distances, revenue, payment mix, and time-of-day demand.

📄 Full terminal transcript (setup → schema → load → queries → results): [`outputs/hive_terminal_output.txt`](outputs/hive_terminal_output.txt)

## Objective
Practice the big-data SQL warehouse workflow end to end: provision Hive, model a table over raw trip records, load a real dataset, and answer operational questions with HiveQL at scale.

## Environment & Approach
- **Engine:** Apache Hive 4.0.0 running in Docker (`apache/hive:4.0.0`, HiveServer2 on ports 10000/10002).
- **Database/table:** `CREATE DATABASE taxi_analysis`; `CREATE TABLE taxidata (vendor_id, pickup_datetime, dropoff_datetime, passenger_count, …)`.
- **Data:** `LOAD DATA LOCAL INPATH '…/yellow_tripdata_2015-01…csv' INTO TABLE taxidata` (NYC TLC Yellow Taxi trips).
- **Analysis:** a series of aggregate HiveQL queries.

## Metrics computed
Total trips; average fare, tip, tax, trip distance, and total trip amount; total revenue, tips, and tolls; tip and toll fractions of revenue; distinct payment types; and pickup-hour demand distribution.

## Business read
Trip-level taxi data answers real operating questions — when demand peaks, how tips and tolls move with fares, and which payment types dominate. Hive makes that queryable at dataset scale with familiar SQL.

## Skills demonstrated
- **Apache Hive / HiveQL** — schema-on-read tables, loads, and analytical SQL over big data.
- **Docker** — provisioning a HiveServer2 environment.
- **Data warehousing** — modeling and aggregating raw records into decision metrics.

## Repository contents
- `outputs/hive_terminal_output.txt` — the complete session: Docker setup, DDL, load, and every query with its results.
