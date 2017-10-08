## ANY and ALL

- used with a WHERE or HAVING clause.

#### The ANY operator returns true if any of the subquery values meet the condition.

```
SELECT column_name(s)
FROM table_name
WHERE column_name operator ANY
(SELECT column_name FROM table_name WHERE condition);
```

#### The ALL operator returns true if all of the subquery values meet the condition.

```
SELECT column_name(s)
FROM table_name
WHERE column_name operator ALL
(SELECT column_name FROM table_name WHERE condition);
```


> 연산자는 표준 비교 연산자임(=, <>, !=, >, >=, <, or <=).



ANY 예시

```
SELECT ProductName 
FROM Products
WHERE ProductID = ANY (SELECT ProductID FROM OrderDetails WHERE Quantity = 10);
```

OrderDetails에서 Quantity가 10인 ProductID를 발췌하여 Products에서 해당하는 ProductName을 나타냄.


ALL 예시

```
SELECT ProductName 
FROM Products
WHERE ProductID = ALL (SELECT ProductID FROM OrderDetails WHERE Quantity = 10);
```

OrderDetails에서 Quantity가 모두 10이어야 하기 때문에 아무것도 나오지 않는다.
