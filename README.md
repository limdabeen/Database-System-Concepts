# Database-System-Concepts
Database-System-Concepts &amp;&amp; Database 수업 정리
### 1️⃣ Database & DBMS 개념
- 데이터: 기록할 만한 가치가 있는 현상, 사건, 아이디어에 대한 묘사
- 데이터베이스(DB): 통합된 영속적 데이터 모음
- DBMS: 데이터를 효율적/편리하게 접근하도록 해주는 시스템

### 2️⃣ 기존 파일 시스템의 한계
- 데이터 중복, 일관성 부족
- 접근 어려움, 프로그램 의존성
- 보안, 무결성, 동시성 문제

### 3️⃣ DBMS의 장단점
- ✅ 장점: 중복 최소화, 공유, 일관성/무결성/보안 유지
- ❌ 단점: 비용, 복잡성, 성능 오버헤드

### 4️⃣ 데이터 추상화와 독립성
- Physical, Logical, View 레벨
- 물리적/논리적 데이터 독립성 확보

---

## 📚 데이터 모델 & 관계 모델

- 데이터 모델 종류: Relational, ER, Object-based, Network, Hierarchical
- 관계 모델 기본 요소:
  - Domain, Attribute, Tuple, Relation
  - Schema vs. Instance
  - Key: Superkey, Candidate Key, Primary Key, Foreign Key
  - NULL의 의미와 특징

---

## 🛠️ 데이터베이스 언어

- **DDL**: 스키마 정의 (ex: CREATE TABLE)
- **DML**: 데이터 조작 (ex: SELECT, INSERT)
- **DCL**: 권한 제어 (ex: GRANT)

---

## 💡 SQL 예시

```sql
-- 고객 이름 조회
SELECT customer_name 
FROM customer 
WHERE customer_id = '192-83-7465';

-- 고객의 계좌 잔고 조회
SELECT account.balance
FROM depositor, account
WHERE depositor.customer_id = '192-83-7465'
  AND depositor.account_number = account.account_number;
