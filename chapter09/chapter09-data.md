# 데이터
    유형, 종속 관계, 계층구조가 존재
    이를 통해서 데이터 모델링을 할 수 있다. 

## 데이터의 유형 
    데이터에는 성격이 유사해서 하나의 틀로 묶을 수 있는 패턴이 있다. 
    데이터 유형을 알면, 데이터를 읽을 수 있다. 

- 업무 데이터
  - 업무과 관련된 사건의 기록
  - 데이터를 육하원칙에 따라 결합한 체계 
  - 주체, 대상, 업무 행위를 통합하고 분리하면 대부분이 아래의 범주에 속한다.

- ![업무 형상화 모델](https://github.com/sendkite/data-modeling/blob/main/chapter09/data-model.png)

<h5>언제, 누가, 무엇, 어떻게와 같은 데이터를 "마스터 데이터"라고 한다.</h5>

업무의 주체, 대상은 성질이 같은 데이터 끼리 통합하고, 업무 행위는 개체 사이의 관계로 표현

---

## 데이터의 종속성과 계층구조 

- 함수적 종속성 -> 정규화 이론 기반 속성간의 종속 관계를 추적
- 개체 수준의 종속성 -> 존재적 관점

### 엔티티
 
- 강한 엔티티 -> 스스로 존재
- 약한 엔티티 -> 상위 엔티티가 있어야 존재 
  - 부모 엔티티의 식별자를 상속받는다.
  - 부모가 삭제되면 같이 삭제된다. 

---

    모든 업무 데이터는 누가 무엇을 언제 어떤 행위를 했다는 기록이다.

### 모든 데이터는 행위, 주체, 대상이 있다.

- ![마스터 데이터](https://github.com/sendkite/data-modeling/blob/main/chapter09/master-data.png)

- 모든 데이터는 육하원칙 중 누가, 무엇을, 언제, 어디서, 어떻게라는 범주를 부모로 하여 발생한다. 
- 활동의 근간이되는 최상위 데이터를 마스터 데이터라 한다. 
- 변경 가능성이 없는 정확성, 일관성이 보장되는 데이터


| 구분  | 설명                        |
|-----|---------------------------|
| 누가  | 모든 인적 자원 (사원, 고객, 협력사)    |
| 무엇을 | 기업의 상품, 서비스. 유 - 무형 자원    |
| 어떻게 | 비지니스 활동의 기준 (계정, 계약, 포인트) |


---
## 데이터 모델링 하기


- ![모델](https://github.com/sendkite/data-modeling/blob/main/chapter09/model.png)

데이터 유형의 관점으로 보면 아래와 같다. 

- ![모델 유형 관점](https://github.com/sendkite/data-modeling/blob/main/chapter09/model-type.png)

### 데이터 유형을 활용해서 데이터 모델링을 행하면 아래와 같다.  

1. 최상위 데이터를 찾는다.
2. 최상위 데이터와 관련된 다른 주체와 대상을 찾는다.
3. 업무 트랜잭션 위주로 찾는다.
4. 트랜잭션의 하위 트랜잭션을 찾는다.
5. 관계를 찾아 연결
6. 각 텐티티의 속성 채우기
7. 모델 상세화

핵심 골격에서 관계있는 하위 엔티티를 만들어간다.
