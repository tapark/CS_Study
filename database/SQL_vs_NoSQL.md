# SQL_vs_NoSQL

### SQL & NoSQL
1. SQL   : 관계형데이터베이스(RDB)를 지칭한다.
2. NoSQL : 관계형데이터베이스가 아닌것.
3. 단순히 SQL문을 사용하고 안하고의 개념이 아닌것에 주의.
4. NoSQL에서도 필요에 따라 SQL문을 사용한다. not only SQL
5. 두개의 비교는 한국인이냐 한국인이아니냐 와 비슷한 개념이다.


### SQL
1. 정형화된 데이터를 처리하기에 좋다.(무결성, 정확성, 중복x)
2. 공통된 쿼리언어와 오픈소스들을 사용하여 다른환경에서도 쉽게 이식 가능하다.
3. 수평적 확장이 어려워서 데이터 처리량의 한계가 생긴다. (수직적 확장 : 컴퓨터 성능을 늘리는 방법)
4. join문이 많은 복잡한 쿼리가 만들어졌을 경우 수정이 어렵다.
5. 데이터베이스 모델링 이후 수정하기 어렵거나 불가능하다. (초기단계에서 개발속도가 느려질수있다.)
6. 가변성이 있는 데이터의 경우 테이블에 저장하기 어렵다.


### NoSQL
1. 비정형화된 데이터를 처리하기에 좋다. (유연함)
2. 가변성이있는 데이터를 저장하기 쉽다.
3. 데이터가 어플리케이션이 요구하는 형태로 저장가능하기때문에 속도가 빠르다 (join문 사용x)
4. 수직적/수평적 확장이 모두가능하여 처리량의 한계가없다.
5. 유연성 때문에 구조결정이 어려울 수 있다.
6. 각각의 쿼리언어를 다르게 사용하는 경우가 많아서 다른환경에 이식하기 어렵다.
7. 데이터가 여러 컬렉션(테이블)에 중복되어있는 경우 모든 컬렉션에서 수정해줘야한다.  


|SQL|MongoDB|DynamoDB|Cassandra|Couchbase|
|---|-------|--------|---------|---------|
|테이블	컬렉션|	테이블|	테이블|	데이터 버킷|
|열|	문서|	항목|	열|	문서|
|컬럼|	필드|	속성|	컬럼|	필드|
|기본 키|	ObjectId|	기본 키| 기본 키|	문서 ID|
|인덱스|	인덱스|	보조 인덱스|	인덱스|	인덱스|
|보기|	보기|	글로벌 보조 인덱스|	구체화된 보기|	보기|
|중첩된 테이블 또는 객체|포함 문서|	맵|	맵|	맵|
|배열|	배열|	목록|	목록|	목록|


|SQL|MongoDB|DynamoDB|Cassandra|Couchbase|
|---|-------|--------|---------|---------|
|Table|	Collection|	Table|	Table|	Data bucket|
|Row|	Document|	Item|	Row|	Document|
|Column|	Field|	Attribute|	Column|	Field|
|Primary key|	ObjectId|	Primary key|Primary key|	Document ID|
|Index|	Index|	Secondary index|	Index|	Index|
|View|	View|	Global secondary index|	Materialized view|	View|
|Nested table or object|	Embedded document|	Map|	Map|	Map|
|Array|	Array|	List|	List|	List|