## INSERT INTO SELECT

#### 하나의 table에서 복사하여 다른 table에 삽입.

- INSERT INTO SELECT requires that data types in source and target tables match
- The existing records in the target table are unaffected



### INSERT INTO SELECT Syntax

#### Copy all columns from one table to another table:

```
INSERT INTO table2
SELECT * FROM table1
WHERE condition;
```


#### Copy only some columns from one table into another table:

```
INSERT INTO table2 (column1, column2, column3, ...)
SELECT column1, column2, column3, ...
FROM table1
WHERE condition;
```

> 몇 개의 column만 복사하는 경우, Null 이 생김.