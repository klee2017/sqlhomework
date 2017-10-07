## INSERT INTO
#### 새로운 record를 삽입할 때.
- 두 가지 방법이 있음.

1. column 이름과 value를 모두 삽입.<br/>
```
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

2. 모든 column에 value만 입력할 때.
(단, 입력 순서대로 value가 들어감.)<br/>
```
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```