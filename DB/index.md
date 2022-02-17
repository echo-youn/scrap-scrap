# Index

## 인덱스를 타지 않는 쿼리 조건

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




## 인덱스를 만들때 NULL을 고려하자

`CREATE INDEX CustPhone_IDX
ON Customers (CustPhoneNumber)
EXCLUDE NULL KEYS;`
  
  
`CREATE INDEX CustPhoneIndex
ON Customers (CustPhoneNumber)
WITH IGNORE NULL;`
  
- SQL SERVER

`CREATE INDEX CustPhone_IDX  
ON Customers (CustPhoneNumber)
WHERE CustPhoneNumber IS NOT NULL;`
 
- MySQL

MySQL은 기본키 컬럼에 널 값을 허용하지 않지만, 인덱스를 만들 때는 모든 널 값이 동일하지 않다고 처리한다. 따라서 널 값이 있는 컬럼에 유일 인덱스를 만들 수 있고, 이 컬럼을 포함한 로우도 여러 개 저장할 수 있다.
MySQL은 인덱스에 널 값을 허용하므로 널 값을 제거하는 옵션이 없다. MySQL에서는 IS NULL과 IS NOT NULL 조건을 검사할 때 인덱스가 있으면 사용한다.
그리고 빈 문자열을 NULL로 변환하지 않는다. NULL 길이를 반환한 결과는 NULL이고, 빈 문자열 길이는 0이다.
  
