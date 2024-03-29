# 객체지향의 사실과 오해

## **부록A** 추상화 기법

사람들이 세계를 이해하는 데 사용하는 중요한 추상화 기법 3가지.

### 분류와 인스턴스화
- 분류(categorize)
  - 공통적인 특성을 가진 특정 객체들의 집합에 공통의 개념을 적용하는 것.
  - 특정한 개념을 나타내는 객체를 집합의 원소로 포함시키는 것.
  - 객체를 타입(개념)과 연관시키는 것. (↔︎ 인스턴스화)
- **타입**을 정의하는 3가지 관점
  - 심볼: 타입을 가리키는 이름
  - 내연: 타입의 정의, 의미
  - 외연: 타입에 속하는 모든 객체들의 집합
  - 도메인을 분석하는 과정에서, 위의 관점들을 이용해 개념을 정의할 수 있다.
- 클래스
  - OOP 언어에서 타입을 구현하는 가장 흔한 방법
  - 동일한 범주(타입)에 속하는 객체는 모두 동일한 속성을 가져야만 한다.


---
### 일반화와 특수화
- 더 일반적인 타입은 슈퍼타입(supertype), 더 특수한 타입은 서브타입(subtype)
- 서브타입은 슈퍼타입이 가진 본질적인 속성과 함께, 자신만의 추가적인 속성을 가진다.
- 어떤 타입의 객체가 특정 속성을 가지고 있음을 알게 되면, 그 하위 타입의 객체들도 그 속성을 가지고 있을 것이라고 논리적으로 추론할 수 있다.
- (외연의 관점에서) 서브타입은 슈퍼타입의 부분집합
- 어떤 타입이 다른 타입의 서브타입이 되기 위해서는 다음을 모두 준수해야 한다 (Larman)
  - 100% 규칙
    - 서브타입은 속성과 연관관계 면에서 슈퍼타입과 100% 일치해야 한다.
  - is-a 규칙 (일반화 관계)
    - 서브타입의 모든 인스턴스는 슈퍼타입 집합에 포함돼야 한다.
    - 즉, 서브타입은 슈퍼타입의 부분집합이다.


---
### 집합과 분해
- 복잡성은 '계층'의 형태를 띤다.
- 집합
  - 안정적인 형태의 부분으로부터 전체를 구축하는 행위
  - 복잡성을 줄일 수 있다.
  - 불필요한 세부사항을 추상화
- 분해
  - 전체를 부분으로 분할하는 행위
- 전체와 부분 간의 일관된 계층 구조는 *재귀적인 설계*를 가능하게 한다.
  - 세부 사항은 무시하고 전체적인 모델을 다룰 수 있다.
  - 필요한 경우에는 내부로 들어가서 세부사항을 확인할 수도 있다.
- 집합은 전체의 내부로 불필요한 세부사항을 감춰주므로, 추상화 매커니즘이면서 캡슐화 매커니즘이다.
- **집합과 분해는 한 번에 다뤄야 하는 요소의 수를 감소시킴으로써, 인지 과부하를 방지한다**.

### 합성 관계
- 합성 관계는 부분을 전체 안에 캡슐화함으로써 인지 과부하를 방지한다.
![image](https://user-images.githubusercontent.com/26949964/70722465-af9f9000-1d3a-11ea-87ce-034cbf5b2086.png)
  - 세부 사항은 무시하고 주문과 상품만이 존재하는 것처럼 모델을 다룰 수 있다.
  - 필요한 경우에는 주문 내부로 들어가서 주문 항목과 관련된 세부 사항을 확인할 수도 있다.
- 따라서 객체들의 그룹과 관련된 복잡성이 완화된다.
- 합성 관계의 경우, 포함하는 객체가 제거되면 그 내부에 포함된 객체도 함께 제거되지만, 연관 관계로 연결된 두 객체는 독립적으로 제거될 수 있다.

### 패키지
- 패키지: 클래스 집합을 하나의 논리적인 단위로 묶는 구성 요소. (= 모듈)
- 개별 클래스가 아닌 클래스의 집합을 캡슐화함으로써, 전체적인 복잡도를 낮춤
- 함께 협력하는 응집도 높은 클래스 집합을 하나의 패키지 내부로 모은다.
- 내부에 포함된 클래스들을 감춤으로써, 시스템 전체의 구조를 추상화한다.