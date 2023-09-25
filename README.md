# 1978. Employees Whose Manager Left the Company
### Problem Link & Description : [ Employees Whose Manager Left the Company](https://leetcode.com/problems/employees-whose-manager-left-the-company/submissions/1054091263/?envType=study-plan-v2&envId=top-sql-50)
## Solution
```sql
/* Write your T-SQL query statement below */
SELECT employee_id
FROM Employees
WHERE salary < 30000
AND manager_id NOT IN (
    SELECT employee_id
    FROM Employees
) ORDER BY employee_id
