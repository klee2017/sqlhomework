## UNION

#### The UNION operator is used to combine the result-set of two or more SELECT statements.

- Each SELECT statement within UNION must have the same number of columns
- The columns must also have similar data types
- The columns in each SELECT statement must also be in the same order



#### UNION Syntax

```
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2;
```


#### UNION ALL Syntax

하나씩만 넣기 때문에 중복을 허용할 때 사용.

```
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2;
```


> Note: result-set에 있는 column 이름은 항상 UNION의 첫 번째 SELECT의 column 이름과 동일함.



- where과 함께 사용할 때 예시.

```
SELECT City, Country FROM Customers
WHERE Country='Germany'
UNION
SELECT City, Country FROM Suppliers
WHERE Country='Germany'
ORDER BY City;
```