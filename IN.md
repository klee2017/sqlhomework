## IN

#### where에 여러 개의 값을 넣고 싶으면 or을 여러 개 쓰는 대신 사용이 가능하다.


예시<br/>
```
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...);
```

또는

```
SELECT column_name(s)
FROM table_name
WHERE column_name IN (SELECT STATEMENT);
```

```
SELECT * FROM Customers
WHERE Country IN ('Germany', 'France', 'UK');
```

`NOT`을 사용하려면 column_name 과 이름 사이에 입력.

중복 적용도 가능하다.

```
SELECT * FROM Customers
WHERE Country IN (SELECT Country FROM Suppliers);
```