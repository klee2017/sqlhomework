## SELECT INTO

#### copies data from one table into a new table.

### SELECT INTO Syntax

#### Copy all columns into a new table:

```
SELECT *
INTO newtable [IN externaldb]
FROM oldtable
WHERE condition;
```


#### Copy only some columns into a new table:

```
SELECT column1, column2, column3, ...
INTO newtable [IN externaldb]
FROM oldtable
WHERE condition;
```


> You can create new column names using the AS clause.


- backup copy를 만들 때:

```
SELECT * INTO CustomersBackup2017
FROM Customers;
```


- 다른 database에 copy를 만들 때:

```
SELECT * INTO CustomersBackup2017 IN 'Backup.mdb'
FROM Customers;
```



- column 몇 개만 새로운 table에 복사할 때:

```
SELECT CustomerName, ContactName INTO CustomersBackup2017
FROM Customers;
```


- where 조건이 있을 때:

```
SELECT * INTO CustomersGermany
FROM Customers
WHERE Country = 'Germany';
```


- 새로운 table에 여러 table에서 발췌하여 복사하고 싶을 때:

```
SELECT Customers.CustomerName, Orders.OrderID
INTO CustomersOrderBackup2017
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID;
```



- 빈 table을 새로 만들려면 query가 no data를 return하게 하는 where을 추가:

```
SELECT * INTO newtable
FROM oldtable
WHERE 1 = 0;
```