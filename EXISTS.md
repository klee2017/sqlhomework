## EXISTS

#### to test for the existence of any record in a subquery.

- returns true if the subquery returns one or more records.



#### EXISTS Syntax

```
SELECT column_name(s)
FROM table_name
WHERE EXISTS
(SELECT column_name FROM table_name WHERE condition);
```

예시

```
SELECT SupplierName
FROM Suppliers
WHERE EXISTS (SELECT ProductName FROM Products WHERE SupplierId = Suppliers.supplierId AND Price < 20);
```


가격이 20 미만인 productname의 supplierID를 가진 SuppliderName만 Supplier에서 발췌.