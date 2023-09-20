# MySQL-Car-Inventory-Analysis

## Car_Dekho Data Analysis

This repository contains SQL queries to analyze car data from the "car_dekho" dataset using MySQL Workbench. The dataset includes information about various cars, such as their year of manufacture, fuel type, and more.

## Prerequisites

Before running the SQL queries, make sure you have:

- Installed MySQL Workbench.
- Created a schema named "cars" and imported the "car_dekho.csv" file.

## Queries

### Total Cars

To get a count of total records in the dataset:

```sql
SELECT count(*) FROM car_dekho;
```

### Cars Available in 2023

To find out how many cars will be available in 2023:

```sql
SELECT count(*) FROM car_dekho WHERE year = 2023;
```

### Cars Available in 2020, 2021, and 2022

To determine the number of cars available in 2020, 2021, and 2022 individually:

```sql
SELECT count(*) FROM car_dekho WHERE year = 2020;
SELECT count(*) FROM car_dekho WHERE year = 2021;
SELECT count(*) FROM car_dekho WHERE year = 2022;
```

### Cars Available in 2020, 2021, and 2022 (Grouped by Year)

To group the count of cars available in 2020, 2021, and 2022 by year:

```sql
SELECT year, count(*) FROM car_dekho WHERE year IN (2020, 2021, 2022) GROUP BY year;
```

### Cars Available by Year

To print the total count of cars by year:

```sql
SELECT year, count(*) FROM car_dekho GROUP BY year;
```

### Diesel Cars in 2020

To find out how many diesel cars will be available in 2020:

```sql
SELECT year, count(*) FROM car_dekho WHERE year = 2020 AND fuel = "Diesel";
```

### Petrol Cars in 2020

To determine how many petrol cars will be available in 2020:

```sql
SELECT year, count(*) FROM car_dekho WHERE year = 2020 AND fuel = "Petrol";
```

### Fuel-wise Car Count by Year

To get the count of petrol, diesel, and CNG cars by year:

```sql
SELECT year, count(*) FROM car_dekho WHERE fuel = "Petrol" GROUP BY year;
SELECT year, count(*) FROM car_dekho WHERE fuel = "Diesel" GROUP BY year;
SELECT year, count(*) FROM car_dekho WHERE fuel = "CNG" GROUP BY year;
```

### Years with More Than 100 Cars

To find the years with more than 100 cars:

```sql
SELECT year, count(*) FROM car_dekho GROUP BY year HAVING count(*) > 100;
```

### Years with Less Than or Equal to 100 Cars

To find the years with less than or equal to 100 cars:

```sql
SELECT year, count(*) FROM car_dekho GROUP BY year HAVING count(*) <= 100;
```

### Years with Less Than or Equal to 50 Cars

To find the years with less than or equal to 50 cars:

```sql
SELECT year, count(*) FROM car_dekho GROUP BY year HAVING count(*) <= 50;
```

### Cars Between 2015 and 2023

To get the count of all cars and their details between 2015 and 2023:

```sql
SELECT count(*) FROM car_dekho WHERE year BETWEEN 2015 AND 2023;
SELECT * FROM car_dekho WHERE year BETWEEN 2015 AND 2023;
```

Feel free to explore these queries to gain insights into the car data. 

Happy analyzing!

