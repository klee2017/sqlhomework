## Comments


#### Single Line


- `--`로 시작함. `--`부터 문장 끝까지 무시됨.


#### Multi-line

- `/*`로 시작해서 `*/`로 끝나고 그 사이에 있는 단어는 무시됨. 문장의 중간에도 사용 가능.


예시

```
SELECT * FROM Customers WHERE (CustomerName LIKE 'L%'
OR CustomerName LIKE 'R%' /*OR CustomerName LIKE 'S%'
OR CustomerName LIKE 'T%'*/ OR CustomerName LIKE 'W%')
AND Country='USA'
ORDER BY CustomerName;
```

중간에 `/*`로 시작해서 `*/`로 끝나는 부분만 무시됨.