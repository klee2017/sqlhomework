## NULL Values

#### A field with a NULL value is a field with no value.

	Note: It is very important to understand that a NULL value is different from a zero value or a field that contains spaces. A field with a NULL value is one that has been left blank during record creation!
	
-  비교 연산자는 사용이 불가하고 IS NULL과 IS NOT NULL 연산자를 대신 사용한다.

#### IS NULL
	SELECT column_names
	FROM table_name
	WHERE column_name IS NULL;
	
#### IS NOT NULL
	SELECT column_names
	FROM table_name
	WHERE column_name IS NOT NULL;