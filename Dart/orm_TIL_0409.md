240409 (Tue)

플러터 과정 27일차

# inheritedWidget
-------------------
InheritedWidget은 Flutter에서 상태를 효과적으로 공유하고 관리하는 방법 중 하나입니다.
InheritedWidget은 위젯 트리를 횡단하여 상위 위젯에서 하위 위젯으로 데이터를 전달하는 데 사용됩니다.
이를 통해 하위 위젯이 필요할 때 상위 위젯의 데이터에 액세스할 수 있게 되며,
이는 상태 관리를 쉽게 하고 코드 구조를 개선하는 데 도움을 줍니다.

왜 필요할까?
widget들을 이용해 화면을 구성했을 때 변화가 필요한 widget이 트리의 끝부분에 있다면 트리의 top부터 bottom까지 불필요한 데이터 이동이 발생한다. 그래서 변화가 필요한 widget의 경우 트리를 통해 내려오는 데이터를 받는 대신, 바로 tree의 top에 접근해 데이터를 가져오게 할 수 잇도록 하는것이다.

![image](https://github.com/BAUu/TIL/assets/44741680/4366fe2e-2a7a-4986-aa6d-6a8001769afb)

### 의존성 주입이란?

어떤 객체가 다른 객체에서 사용되도록 하는 것
생성자를 통해 필요한 객체를 전달하는 것이 일반적
생성자를 통한 의존성 주입은 의존성 트리가 깊어질수록 단계를 많이 타야되는 단점이 있음

InheritedWidget은 이런 단점을 해소

MediaQuery
Theme

**InheritedWidget : 의존성 주입용 위젯**
**BuildContext : 위젯 트리 정보를 알고 있는 객체 (신)**
  이거 없으면 화면 이동도 못 함
  이거 없으면 다이얼로그도 실행 안 됨

플러터 공식 유튜브
https://youtu.be/og-vJqLzg2c
