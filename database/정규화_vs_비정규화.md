# 정규화 데이터베이스(normalized database)
 - 중복을 최소화하도록 설계된 데이터베이스 -> join을 활용
# 비정규화 데이터베이스(denormalized database)
 - 읽는 시간을 최적화하도록 설계된 데이터베이스 -> join을 최소화

### 졍규화 데이터베이스는 중복을 최소화 한다.
1. 안정성과 무결성 보장
2. 저장공간의 최소화
3. 효과적인 검색 알고리즘 생성가능
4. 데이터 삽입시 릴레이션 재구성의 필요성 감소

### 비정규화 데이터베이스는 읽는 시간을 최적화한다.
1. 빠른 데이터 조회 (join이 적다)
2. 무결성이 깨질 수 있다. -> 이상(Anomaly)현상 발생
3. 데이터를 중복 저장하므로 저장공간이 필요
4. 데이터 갱신이나 삽입 비용이 높음

### 중복된 정보로 인해 발생하는 문제들을 이상 현상(Anomaly)이라 말한다.
- 삽입 이상(Insertion Anomaly) : 원하지 않는 자료가 삽입된다든지, 삽입하는데 자료가 부족해 삽입이 되지 않아 발생하는 문제점을 말한다.
- 삭제 이상(Deletion Anomaly) : 하나의 자료만 삭제하고 싶지만, 그 자료가 포함된 튜플 전체가 삭제됨으로 원하지 않는 정보 손실이 발생하는 문제점을 말한다.
- 갱신 이상(Modification Anomaly) : 정확하지 않거나 일부의 튜플만 갱신되어 정보가 모호해지거나 일관성이 없어져 정확한 정보 파악이 되지 않는 문제점을 말한다.

→ 이상 현상은 정규화를 통해 방지할 수 있다.