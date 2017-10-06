## SQL AND, OR and NOT Operators

- AND: 모든 조건이 참일 때.
- OR: 여러 조건 중 하나가 참일 때.
- NOT: 조건이 참이 아닐 때.

#### AND

```
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
```

#### OR

```
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
```

#### NOT

```
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
```