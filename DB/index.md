# Index

인덱스를 타지 않는 쿼리 조건

### LIKE 검색시 좌변에 %를 붙일 경우
----

`SELECT * 
FROM PEOPLE
WHERE NAME LIKE '%승재...'`
 

### IS NULL이나 IS NOT NULL을 사용할경우
----
`SELECT *
FROM PEOPLE
WHERE NAME IS NULL`

### 인덱스로 지정된 칼럼이 가공되거나 변형된 경우
----
`SELECT *
FROM PEOPLE
WHERE SUBSTR(NAME, 0, 3)`

### 부정연산자(!=, <>)를 사용하는 경우
----
`SELECT *
FROM PEOPLE
WHERE NAME != '승재'`

### 암시적인 형변환
----
`SELECT *
FROM PEOPLE
WHERE AGE = '20'` ## 다른 형으로 값을 비교하고 있음
