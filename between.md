## BETWEEN

#### 주어진 범위 내의 값을 선택하는 연산자. 숫자, 문자, 날짜가 가능하며 처음 값과 마지막 값이 포함된다.

예시<br/>
```
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2;
```

그 반대의 값들을 얻고 싶을 땐 `between` 대신 `not between`을 이용한다.

중복 사용 예시<br/>
```
SELECT * FROM Products
WHERE (Price BETWEEN 10 AND 20)
AND NOT CategoryID IN (1,2,3);
```

문자 사용 예시<br/>
```
SELECT * FROM Products
WHERE ProductName BETWEEN 'Carnarvon Tigers' AND 'Mozzarella di Giovanni'
ORDER BY ProductName;
```
