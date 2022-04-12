# chapter10
## Account 개체 그룹핑 모델링

Account란 무엇일까?

업무 행위의 최상위 주체로, 관련 업무를 동일한 성격으로 관리하는 단위.


업무의 최상의 주체를 찾아야한다. 

EX) 가족의 휴대폰 요금

- 주체: 아빠, 엄마, 아들
- 대상 : 휴대폰 요금 청구 
- 요구사항 : 아들은 미성년자라 엄마한테 엄마, 아들 비용을 통합해서 청구하고 싶다. 

- 여기서 다수의 가족원을 묶어서 청구해주는 "최상위 주체"는 청구 계정이다. 


- ![엔티티](https://github.com/sendkite/data-modeling/blob/main/chapter10/phone-entity.png)


아래와 같은 그룹 관계로 최상위 주체 "Account"를 정의할 수 있다.

- ![그룹 관계](https://github.com/sendkite/data-modeling/blob/main/chapter10/mannytomanny.png)