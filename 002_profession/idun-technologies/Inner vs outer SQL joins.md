#core/softwaredevelopment

SQL joins combine rows from two or more tables based on related columns. The **type of join determines which rows are included** when matches are missing.

## Inner Join

- **Returns only rows with matching values in both tables**
- Non-matching rows are excluded entirely
- Most restrictive join type

> [!example] Inner Join
> ```sql
> SELECT employees.name, departments.dept_name
> FROM employees
> INNER JOIN departments ON employees.dept_id = departments.id;
> ```
> Result: Only employees who belong to an existing department.

## Outer Joins

Outer joins **retain rows even when no match exists**, filling gaps with `NULL`.

### Left Outer Join

- Returns **all rows from the left table**
- Matching rows from right table (or `NULL` if no match)

### Right Outer Join

- Returns **all rows from the right table**
- Matching rows from left table (or `NULL` if no match)

### Full Outer Join

- Returns **all rows from both tables**
- `NULL` where no match exists on either side

> [!example] Left Join
> ```sql
> SELECT employees.name, departments.dept_name
> FROM employees
> LEFT JOIN departments ON employees.dept_id = departments.id;
> ```
> Result: All employees, including those without a department (shown as `NULL`).

## Comparison

| Join Type | Left Table | Right Table | Use Case |
|-----------|------------|-------------|----------|
| Inner | Matched only | Matched only | Strict relationships |
| Left | All rows | Matched or NULL | Primary table + optional data |
| Right | Matched or NULL | All rows | Secondary table focus |
| Full | All rows | All rows | Complete data audit |

## When to Use

- **Inner**: When you only want complete, matching records
- **Left**: When the left table is your "source of truth"
- **Right**: Rarely used; restructure query to use Left instead
- **Full**: Data reconciliation, finding orphaned records
