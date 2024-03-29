# 06 객체 지도

> 유일하게 변하지 않는 것은 모든 것이 변한다는 사실 뿐이다 - 헤라클레이토스

- 다른 사람에게 길을 물어보는 방법은 '기능적이고 해결책 지향적인 접근법' 이다.
  - 길을 가르쳐 주는 사람은 어디~어디~어디~로 가시면 뭐가 나오고 어디로 가면 어쩌고 저쩌고
  - 이 방법은 일반적이지도 , 재사용 가능하지도 않다.
  - 강이나 산과 같은 중요한 랜드마크(지표)가 없다면 설명이 어렵다
  - 현재의 요구만을 만족


- 지도는 실세계의 지형을 기반으로 추상화된 모델이다.
  - 길을 찾는데 필요한 모든 정보가 지도 안에 포함돼 있기 때문에 길을 구구절절 설명할 필요가 읍다
  - 현재의 목적 뿐만 아니라 다양한 목적을 위해 재사용 될 수 있다. 범용적이다.

- 길을 직접 알려주는 방법이 기능적이고 해결 방법 지향적인 접근법이라면, 지도를 이용하는 방법은
'구조적이고 문제 지향적인 접근법'이다.

- 지도는 길을 찾는 데 필요한 구체적인 기능이 아니라 길을 찾을 수 있는 '구조'를 제공한다.
  - 기능에 대한 요구사항이 계속 변함에도 지도는 모든 요구사항을 수용할 수 있다.


- 기능을 중심으로 구조를 종속시키는 접근법은 범용적이지 않고 재사용이 불가능하며 변경에 취약한 모델을 낳게 된다.

- 객체지향 개발 방법은 안정적인 구조에 변경이 빈번하게 발생하는 기능을 종속시키는 지도의 방법과 유사
  - 범용적, 높은 재사용성, 변경에 안정적
  - 즉, 객체지향은 자주 변경되는 기능이 아니라 안정적인 구조를 기반으로 시스템을 구조화한다

## 기능 설계 대 구조 설계

설계의 가장 큰 도전은 기능과 구조라는 두가지 측면을 함께 녹이는 것이다

- 기능 설계
  - 사용자를 위해 무엇을 할 수 있는지에 초점을 맞춘다

- 구조 설계
  - 형태가 어떠한가에 초점을 맞춘다

- 요구사항의 변경은 피할 수 없기 때문에 요구사항 변경에 유연하게 대처할 수 있는 안정적인 구조가 필요하다

- 설계가 어려운 이유는 어제 약속했던 기능을 제공하는 동시에 내일 변경될지도 모르는 요구사항도 수용할 수 있는 코드를 창조해야 하기 때문이다

- 불확실한 미래의 변경을 예측하고 성급하게 설계에 반영하는 것은 불필요하게 복잡한 설계를 낳을 뿐이다
  - 변경을 예측하지 말고, 변경을 수용할 수 있는 선택의 여지를 설계에 마련해 놓는 것이 중요

- 객체 지향은 객체의 구조에 집중하고 기능이 객체의 구조를 따르게 만든다
  - 시스템 기능은 더 작은 책임으로 분할되고 적절한 객체에게 분배되기 때문에 기능이 변경되더라도 객체 간의 구조는 그대로 유지된다
  - 객체를 기반으로 책임과 역할을 식별하고 메시지를 기반으로 객체들의 협력 관계를 구축하는 이유다


## 두 가지 재료 : 기능과 구조

객체지향 세계를 구축하기 위해서는 사용자에게 제공할 **기능**과 기능을 담을 안정적인 **구조**라는 재료가 준비돼야 한다

- 구조 : 사용자나 이해관계자들이 도메인에 관해 생각하는 개념과 개념들 간의 관계로 표현한다
- 기능 : 사용자의 목표를 만족시키기 위해 책임을 수행하는 시스템의 행위로 표현한다

## 안정적인 재료 : 구조

### 도메인 모델

사용자가 프로그램을 사용하는 대상 분야를 도메인 이라고 한다

- 도메인 모델
  - 모델이란 대상을 단순화해서 표현한 것이다
  - 모델은 지식을 선택적으로 단순화하고 의식적으로 구조화한 형태
  - 모델은 중요한 문제에 집중할 수 있도록 필요한 지식만 재구성 한 것이다
  - 대상을 추상화, 단순화한 것이다
  - 모델을 사용하면 현재의 문제와 관련된 측면은 추상화하고, 그 밖에 관련없는 세부 사항은 무시할 수 있다
  - 도메인 모델은 소프트웨어가 목적하는 영역 내의 개념과 개념간의 관계, 다양한 규칙이나 제약등을 주의깊게 추상화한 것이다

### 도메인의 모습을 담을 수 있는 객체지향

- 최종 코드는 사용자가 도메인을 바라보는 관점을 반영해야 한다
  - 곧 애플리케이션이 도메인 모델을 기반으로 설계돼야 한다는 것을 의미

- 객체지향을 이용하면 도메인에 대한 사용자 모델, 디자인 모델, 시스템 이미지 모두가 유사한 모습을 유지하도록 만드는 것이 가능하다
  - 객체지향의 이러한 특징을 **연결완전성** 또는 **표현적차이** 라고 한다

### 표현적 차이

- 소프트웨어 객체는 현실 객체를 모방한 것이 아니라 은유를 기반으로 재창조한 것이다
- 소프트웨어 객체와 현실 객체 사이의 의미적 거리를 가리켜 표현적 차이, 의미적 차이라 한다
- 핵심은 은유를 통해 현실 객체와 소프트웨어 객체 사이의 차이를 최대한 줄이는 것이다
- 사용자가 도메인에 대해 생각하는 개념을 은유를 통해 투영해야 한다
- 즉 소프트웨어 객체를 창조하기 위해 우리가 은유해야 하는 대상은 바로 도메인 모델이다


## 불안정한 재료 : 기능

### 유스케이스

- 기능적 요구사항이란 시스템이 사용자에게 제공해야 하는 기능의 목록을 정리한 것이다
- 사용자의 목표를 달성하기 위해 **사용자와 시스템 간에 이뤄지는 상호작용**의 흐름을 텍스트로 정리한 것을 유스케이스 라고 한다

- 유스케이스의 특성
  - 유스케이스는 사용자와 시스템 간의 상호작용을 보여주는 텍스트다
    - 유스케이스는 다이어그램이 아니다
    - 유스케이스의 핵심은 사용자와 시스템 간의 상호작용을 일련의 이야기 흐름으로 표현한 것
  - 유스케이스는 하나의 시나리오가 아닌 여러 시나리오들의 집합이다
    - 시나리오는 유스케이스를 통해 시스템을 사용하는 하나의 특정한 이야기 또는 경로다
    - 유스케이스는 하나의 시나리오가 아니라 이자액 계산 이라는 사용자의 목표와 관련된 모든 시나리오의 집합이다
  - 유스케이스는 단순한 피처 목록과 다르다
    - 피처는 시스템이 수행해야 하는 기능의 목록을 단순하게 나열한 것이다
    - 유스케이스의 강점은 유스케이스가 단순히 기능을 나열하는 것이 아니라 이야기를 통해 연관된 기능들을 함께 묶을 수 있다는 점이다
  - 유스케이스는 사용자 인터페이스와 관련된 세부 정보를 포함하지 말아야 한다
    - 유스케이스는 자주 변경되는 사용자 인터페이스 요소는 배제하고 사용자 관점에서 시스템의 행위에 초점을 맞춘다
  - 유스케이스는 내부 설계와 관련된 정보를 포함하지 않는다
    - 연관된 시스템의 기능을 모으는 것이지 내부 설꼐를 설명하는 것이 아니다

### 유스케이스는 설계 기법도, 객체지향 기법도 아니다

- 유스케이스는 사용자가 바라보는 시스템의 외부 관점만을 표현한다
- 유스케이스는 단지 기능적 요구사항을 사용자의 목표라는 문맥을 중심으로 묶기 위한 정리 기법일 뿐.


## 재료 합치기 : 기능과 구조의 통합

### 도메인 모델, 유스케이스, 그리고 책임주도설계

- 도메인 모델은 안정적인 구조를 개념화 하기 위해 사용되는 도구
- 유스케이스는 불안정한 기능을 서술하기 위해 사용되는 도구다
- 변경에 유연한 소프트웨어를 만들기 위해서는 유스케이스에 정리된 시스템의 기능을 도메인 모델을 기반으로 한 객체들의 책임으로 분배해야 한다

- 협력의 출발을 장식하는 첫 번째 메시지는 시스템의 기능을 시스템의 책임으로 바꾼후 얻어진 것이다??

- 시스템에 할당된 커다란 책임은 시스템안의 작은 규모의 객체들이 수행해야 하는 작은 규모의 책임으로 세분화 된다
  - 어떤 객체를 선택할 것인가? 도메인 모델이 필요하다
  - 도메인 모델에 포함된 개념을 은유하는 소프트웨어 객체를 선택해야 한다

---
### 객체 설계는 다음과 같이 표현되기도 한다
요구사항들을 식별하고 도메인 모델을 생성한 후, 소프트웨어 클래스에 메서드들을 추가하고, 요구사항을 충족시키기 위해 객체들 간의 메시지 전송을 정의하라.
---


- 유스케이스는 사용자에게 제공할 기능을 시스템의 책임으로 보게 함으로써 객체간의 안정적인 구조에 책임을 분배할 수 있는 출발점을 제공한다
- 도메인 모델은 기능을 수용하기 위해 은유할 수 있는 안정적인 구조를 제공한다
- 책임-주도 설계는 유스케이스로부터 첫 번째 메시지와 사용자가 달성하려는 목표를, 도메인 모델로부터 기능을 수용할 수 있는 안정적인 구조를 제공받아 실제로 동작하는 객체들의 협력 공동체를 창조한다

- 책임-주도 설계는 유스케이스와 도메인 모델을 통합한다
- 중요한 것은 견고한 객체지향 애플리케이션을 개발하기 위해서는 사용자의 관점에서 시스템의 기능을 명시하고, 사용자와 설계자가 공유하는 안정적인 구조를 기반으로 기능을 책임으로 변환하는 체계적인 절차를 따라야 한다는 것이다

- 도메인 모델에 명시된 정기예금,계좌와 같은 개념을 스스로 상태와 행위를 관리하는 자율적 객체로 간주한다
- 각 객체는 자신의 책임을 완수하는데 필요한 정보나 서비스가 필요한 경우 다른 객체에게 책임을 요청한다
- 따라서 시스템의 기능은 역할과 책임을 수행하는 객체들의 협력관계를 통해 구현된다

- 책임할당의 기본 원칙은 책임을 수행하는데 필요한 정보를 가진 객체에게 그 책임을 할당하는 것이다
  - 이것은 관련된 상태와 행동을 함께 캡슐화 하는 자육적인 객체를 낳는다(상태와 행위의 캡슐화 ch.5)

### 기능 변경을 흡수하는 안정적인 구조

- 도메인 모델을 구성하는 개념은 비즈니스가 없어지지 않는한 안정적으로 유지된다
- 도메인 모델을 구성하는 개념 간의 관계는 비즈니스 규칙을 기반으로 한다
  - 비즈니스 정책이 변경되지 않는 한 안정적으로 유지된다

- 객체지향의 가장 큰 장점은 도메인을 모델링하기 위한 기법과 도메인을 프로그래밍 하기 위해 사용하는 기법이 동일하다는 것
  - 도메인 모델링에서 프로그래밍 설계에서의 객체와 클래스로 변환할 수 있다.
  - 이를 연결완전성 이라고 한다

- 사람들이 동일한 용어와 동일한 개념을 이용해 의사소통하고 코드로부터 도메인 모델을 유추할 수 있게 하는 것이 도메인 모델의 진정한 목표다

## 정리
- 안정적인 도메인 모델을 기반으로 시스템의 기능을 구현하라
- 도메인 모델과 코드를 밀접하게 연관시켜라
- 그러면 유지보수하기 쉽고 유연한 객체지향 시스템을 만드는 첫걸음이 될것이다.

