# SQL Injection
SQL 인젝션(SQL 삽입, SQL 주입으로도 불린다)은 코드 인젝션의 한 기법으로 클라이언트의 입력값을 조작하여 서버의 데이터베이스를 공격할 수 있는 공격방식을 말한다. 주로 사용자가 입력한 데이터를 제대로 필터링, 이스케이핑하지 못했을 경우에 발생한다.

~~SQL
INSERT INTO students (이름) VALUES ('학생 이름');
~~~
여기서 Robert'); DROP TABLE students;-- 을 "학생 이름" 자리에 넣을 경우 다음과 같은 명령문이 된다.
~~SQL
INSERT INTO students (이름) VALUES ('Robert');
DROP TABLE students;
--');
~~~
첫 번째 줄에서는 Robert라는 학생이 입력되었지만, 두 번째 줄에서 학생들의 데이터가 있는 테이블을 제거한다. 그리고 세 번째에서는 뒤에 오는 내용을 모두 주석 처리한다. 결과적으로 ‘모든 학생 기록을 삭제한다.’라는 뜻의 명령문이 완성된다.