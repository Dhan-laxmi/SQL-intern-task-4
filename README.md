# SQL Developer Internship - Task 4: Aggregate Functions & Grouping

## Objective
Use aggregate functions (`SUM`, `AVG`, `COUNT`, `MIN`, `MAX`) along with `GROUP BY` and `HAVING` to summarize and analyze flight data.

---

##  Tools
- MySQL Workbench

---

## Files in this repository
- **flights_table.sql** → Contains:
  - Table creation script for `flights`
  - Sample flight records
  - SQL queries using aggregate functions & grouping

---

## Dataset Structure

| Column            | Type    | Description |
|-------------------|---------|-------------|
| flight_id         | INTEGER | Unique flight ID |
| airline           | TEXT    | Airline name |
| origin            | TEXT    | Starting city |
| destination       | TEXT    | Destination city |
| distance_km       | INTEGER | Distance in kilometers |
| duration_minutes  | INTEGER | Flight duration in minutes |
| ticket_price      | REAL    | Price per ticket (₹) |
| passengers        | INTEGER | Number of passengers on the flight |

---

## 📋 Example Queries

 **Total passengers carried by each airline**
```sql
SELECT airline, SUM(passengers) AS total_passengers
FROM flights
GROUP BY airline;
