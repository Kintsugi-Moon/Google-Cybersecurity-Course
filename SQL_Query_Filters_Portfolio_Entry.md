# SQL Query Portfolio: Apply Filters to SQL Queries

## Project Description

This project simulates a real-world cybersecurity investigation scenario where SQL queries are used to analyze user login activity and employee data to detect potential security incidents. By applying filters using logical operators, date and time constraints, and pattern matching, we demonstrate how SQL can be leveraged for detailed data inspection. This portfolio showcases several essential queries that help isolate suspicious activity, which is a key skill for any cybersecurity analyst.

---

## Retrieve After-Hours Failed Login Attempts

### SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE success = 0 AND login_time > '18:00:00';
```

### Explanation

This query returns all failed login attempts (where success = 0) that occurred after 6:00 PM. It filters the `log_in_attempts` table using the `AND` operator and a time condition.

---

## Retrieve Login Attempts on Specific Dates

### SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';
```

### Explanation

This query helps identify login attempts that occurred on May 8 and May 9, 2022. This is useful when investigating suspicious activities that might span multiple days.

---

## Retrieve Login Attempts Outside of Mexico

### SQL Query

```sql
SELECT *
FROM log_in_attempts
WHERE country NOT LIKE '%MEX%';
```

### Explanation

This query filters out login attempts that originated from Mexico by excluding rows where the `country` column includes either 'MEX' or 'MEXICO'. The `LIKE` keyword with `%` is used to account for partial matches.

---

## Retrieve Employees in Marketing (East Building Only)

### SQL Query

```sql
SELECT *
FROM employees
WHERE department LIKE '%Marketing%'
AND office LIKE 'East%';
```

### Explanation

This query retrieves all employees in the Marketing department whose office is located in the East building. Both `LIKE` filters use `%` to capture partial matches.

---

## Retrieve Employees in Finance or Sales

### SQL Query

```sql
SELECT *
FROM employees
WHERE department LIKE '%Finance%' OR department LIKE '%Sales%';
```

### Explanation

This query identifies all employees who work in either the Finance or Sales department using the `OR` logical operator.

---

## Retrieve All Employees Not in IT

### SQL Query

```sql
SELECT *
FROM employees
WHERE department NOT LIKE '%Information Technology%';
```

### Explanation

This query retrieves all employees who are not in the Information Technology department. The `NOT LIKE` clause filters out entries containing 'Information Technology'.

---

## Summary

In this project, we used SQL to investigate a variety of potential security issues. We wrote queries to find failed logins after business hours, identify login attempts on specific dates, and exclude specific countries from our results. We also filtered employee data to support security updates across different departments. This exercise demonstrates how SQL filtering capabilities can support real-world cybersecurity investigations, making it a valuable addition to any analyst’s toolkit.

---

## Notes

All queries were typed directly into this portfolio as permitted by the assignment instructions. Screenshots were omitted.
