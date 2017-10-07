## LIKE

#### where을 이용하여 column에서 특별한 패턴을 찾을 때.

- `%`는 하나 이상의 문자를 나타낼 때 함께 사용하고 `_`는 한 개의 문자를 나타낼 때 함께 사용. 이 둘은 함께 사용 가능함.

> Note: MS Access uses a question mark (?) instead of the underscore (_).

```
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```

예시<br/>
![wildcard_like](./img/wildcard_like.png)


