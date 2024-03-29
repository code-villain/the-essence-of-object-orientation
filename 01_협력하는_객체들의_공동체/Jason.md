# 객체지향의 사실과 오해
## 1장 협력하는 객체들의 공동체

### *역할, 책임, 협력*

1. **협력**
    - 요청과 응답으로 구성
    - 하나의 문제를 해결하기 위해 여러 객체에게 요청한다.
        - 한 객체에 대한 요청이 다른 객체에 대한 요청을 유발하는 일이 일반적이다.
        - 요청이 연쇄적으로 발생한다.
    - 요청을 받은 객체는 주어진 책임을 다하면서 요청에 응답한다.
    - 요청이 연이어 발생하므로 응답 역시 연쇄적으로 전달된다.

2. **역할과 책임**
    - 여러 객체가 동일한 역할을 수행할 수 있다.
    - 역할은 대체 가능하다.
    - 책임을 수행하는 방법은 자율적으로 선택할 수 있다.
    - 하나의 객체가 동시에 여러 역할을 수행할 수 있다.
    
### *협력 속에 사는 객체*

1. 협력 공동체로서 객체가 갖춰야할 두 가지 덕목
    - 객체는 **협력적**이어야 한다.
        * 객체는 다른 객체에게 적극적으로 요청할 정도의 열린 마음이 있어야한다.
        * 모든 것을 스스로 처리하려하는 전지전능한 객체(god object)는 내부 복잡도로 자멸하고 만다.
        * 객체는 다른 객체의 명령에 복종하는 것이 아닌 요청에 응답할 뿐이며 어떤 식으로 응답할지는 객체 스스로 판단한다.
    - 객체는 **자율적**이어야 한다.
        * 객체는 다른 객체와 협력할 수 있을 만큼 개방적인 동시에 협력에 참여하는 방법을 스스로 결정할 수 있을 만큼 충분히 자율적이어야 한다.
2. **상태**와 **행동**을 지닌 자율적인 객체

    > 객체는 다른 객체가 '무엇(what)'을 수행하는 지는 알 수 있지만 '어떻게(how)' 수행하는지는 알 수 없다.
    - 객체가 협력에 참여하기 위해 어떤 행동을 해야 한다면 그 행동에 필요한 상태도 함께 있어야 한다.
3. 협력과 메시지
    - 객체는 협력을 위해 다른 객체에게 메시지를 전송하고 다른 객체로부터 메시지를 수신한다.
4. 메서드와 자율성
    - **메서드**
        * 객체가 수신된 메시지를 처리하는 방법
    - 메서드와 메시지의 분리
        * 외부의 요청을 표현하는 메시지와 요청을 처리하기 위한 메서드를 분리하는 것은 객체의 자율성을 높인다. 이는 캡슐화와도 큰 연관이 있다.

### *객체지향의 본질*
1. 객체지향이란 시스템을 상호작용하는 **자율적인 객체들의 공동체**로 바라보고 객체를 이용해 시스템을 분할하는 방법
2. 자율적인 객체란 **상태**와 **행위**를 함께 지니며 스스로 자기 자신을 책임지는 객체
3. 객체는 시스템의 행위를 구현하기 위해 다른 객체와 **협력**한다. 각 객체는 협력 내에서 정해진 **역할**을 수행하며 역할은 관련된 **책임**의 집합이다.

---

### 회고
> 객체가 자율적이어야 한다는 말이 잘 이해가 되지 않았다. 
>사람의 입장에서 생각하면 객체는 사람이 만들고(인스턴스화 얘기가 아니다 ㅡ.ㅡ) 객체를 실제로 사용하는 주체는 다른 객체이다. 
>도대체 어디가 자율적이라는 건가하고 생각했다가 사람을 배제하고 객체와 객체간의 관계에서 생각해보니 객체는 다른 객체에게 메시지를 전달할 수는 있지만 그 객체가 어떤 상태를 가지고 있는지 어떤 행동을 취할지는 직접적으로 알 수 없다. 
>아마 **캡슐화**를 설명하려고 저런 표현이 나온게 아닌가 싶다.
>
>객체는 다른 객체가 '무엇(what)'을 수행하는 지는 알 수 있지만 '어떻게(how)' 수행하는지는 알 수 없다. 이 표현이 결정적이었다