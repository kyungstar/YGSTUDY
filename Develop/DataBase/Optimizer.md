# 옵티마이저
- 가장 효율적인 방법으로 SQL을 수행할 최적의 처리 경로를 생성해주는 DBMS 핵심 엔진
- 컴퓨터의 두뇌가 CPU인 것처럼 DBMS의 두뇌는 옵티마이저라고 할 수 있다.
- 개발자가 SQL을 작성하고 실행하면 즉시 실행되는 것이 아니라, 옵티마이저가 실행 계획을 세우게 된다.

ㄴ 실행 계획을 세운 후 시스템 통계 정보를 활용하여 각 실행 계획의 예상 비용을 산정한다.

ㄴ 이후, 각 실행 계획을 비교해서 최고의 효율을 가지고 있는 실행 계획을 판별한다.

ㄴ 최적의 실행계획에 따라 쿼리를 수행하게 된다.


---



### 쿼리의 실행 속도와 성능을 최적화하기 위해 다음과 같은 작업을 수행하는 옵티마이저의 역할


#### 1. 쿼리 분석(Statement Parsing):

- 옵티마이저는 사용자가 입력한 SQL 문을 분석하여 문법 검사 및 의미 분석을 수행한다.
- 이 단계에서 문장의 구조와 의미를 이해하고 데이터베이스 객체(테이블, 인덱스 등)와 관련된 정보를 수집한다.

#### 2. 실행 계획 생성(Execution Plan Generation):

- 옵티마이저는 쿼리를 실행하기 위한 다양한 실행 계획을 생성한다.
- 실행 계획은 쿼리를 처리하기 위한 접근 경로, 조인 방법, 인덱스 사용 등의 세부 정보를 포함한다.
- 가능한 모든 실행 계획을 고려하고, 비용 기반 최적화(Cost-Based Optimization)라는 기법을 사용하여 각 실행 계획의 예상 비용을 평가한다.


#### 3. 실행 계획 평가(Execution Plan Evalution):

- 옵티마이저는 생성된 실행 계획 중에서 가장 비용이 적은 최적의 실행 계획을 선택한다.
- 비용은 I/O비용, CPU 비용, 메모리 사용량 등의 요소를 고려하여 계산된다.
- 최적의 실행 계획은 쿼리의 처리 속도를 최대화하고, 자원 사용을 최소화하여 효율적인 실행을 달성한다.


#### 4. 실행 계획 실행(Execution Plan Execution):
- 옵티마이저가 선택한 최적의 실행 계획에 따라 데이터베이스 엔진이 쿼리를 실행한다.
- 이 단계에서 데이터베이스는 필요한 데이터를 액세스하고 조작하여 쿼리 결과를 생성한다.

```
[출처]
 1. DB Optimizer(옵티마이저)|작성자 Sodam 
```