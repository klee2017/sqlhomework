## GROUP BY

#### to group the result-set by one or more columns.


#### GROUP BY Syntax

```
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
```


예시

```
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country;
```

위와 같이 입력하면 나라별로 CustomerID의 갯수를 나타냄.



```
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
ORDER BY COUNT(CustomerID) DESC;
```


CustomerID의 갯수를 토대로 역순으로 정렬.



Join과 함께 사용.

```
SELECT Shippers.ShipperName,COUNT(Orders.OrderID) AS NumberOfOrders FROM Orders
LEFT JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID
GROUP BY ShipperName;
```