# 7장 함께모으기

- 마틴 파울러가 이야기 하는 객체지향 설계안에 존재하는 세가지 상호 연관된 관점
    1. 개념관점 -> (사용자가 생각하는) 도메인
    2. 명세관점 -> 인터페이스 
    3. 구현관점 -> 구현 코드
    - 1번은 사용자에 가깝고 3번은 개발자에 가깝군

- 도메인 모델 먼저 생각해보고, 그 도메인 모델간 (혹은 객체간) 어떤 협력 어떤 메시지가 있어야 하는지 생각한다. **1순위가 협력관 메시지**다.

- 계속 예시가 보여주는건 메시지를 먼저 생각하고, 이 메세지를 수행할 적절한 객체를 사용한다. 여기서 적절한 객체는 도메인 모델에서 가져온다.

- 214쪽 "객체지향 설계의 첫 번째 목표는 훌륭한 객체를 설계한느 것이 아니라 훌륭한 협력을 설계한느 것이라는 점을 잊지 말자"

- 222쪽 하단, 항상 구현중에 인터페이스가 바뀌면 마음이 불편했다. 제대로 된 명세를 하지 못했다는 자책이 생겼는데 아주 자연스러운 일이라니 ㅎㅎ

- 228쪽 "다시 한번 강조한다. 인터페이스와 구현을 분리하라." - 본인은 서비스 레이어에서 안하심 ㅋㅋㅋㅋ