## IFNULL(), ISNULL(), COALESCE(), and NVL()

- 어떤 column에 null이 있는 경우, 그 data를 이용하여 계산한 값도 null이 되기 때문에 이를 해결하기 위해.

### MySQL

#### IFNULL()을 이용하여 다른 값으로 대체함.

```
SELECT ProductName, UnitPrice * (UnitsInStock + IFNULL(UnitsOnOrder, 0))
FROM Products
```

- UnitsOnOrder를 0으로 대체.


#### COALESCE()를 이용

```
SELECT ProductName, UnitPrice * (UnitsInStock + COALESCE(UnitsOnOrder, 0))
FROM Products
```

- COALESCE() 안에 있는 list 값들 중 null이 아닌 값을 return.


### SQL Server

#### ISNULL()을 이용하여 다른 값으로 대체.

```
SELECT ProductName, UnitPrice * (UnitsInStock + ISNULL(UnitsOnOrder, 0))
FROM Products
```



### MS Access

#### IsNull()을 이용하여 null이면 TRUE(-1)를 return하고, 아니면 FALSE(0)를 return.

```
SELECT ProductName, UnitPrice * (UnitsInStock + IIF(IsNull(UnitsOnOrder), 0, UnitsOnOrder))
FROM Products
```


### Oracle

#### NVL()

```
SELECT ProductName, UnitPrice * (UnitsInStock + NVL(UnitsOnOrder, 0))
FROM Products
```