# 객체지향의 5가지 원칙(SOILD)

### 역사와 필요성

객체지향 5가지 원칙(SOLID)은 1990년대 중반에 로버트 마틴(Robert C. Martin)이 제안한 것으로, 객체지향 개발에서 소프트웨어의 유지보수성과 확장성을 높이기 위해 만들어졌습니다.

객체지향 프로그래밍은 소프트웨어를 객체 단위로 모델링하여 개발하는 방법입니다. 객체지향 프로그래밍은 상속, 캡슐화, 다형성 등의 특징을 가지며, 객체지향 설계는 이러한 특징을 바탕으로 객체 간의 관계를 설계합니다.

하지만, 객체지향 개발에서도 소프트웨어 개발의 복잡성과 유지보수성을 해결하기 위한 방법이 필요했습니다. 이를 위해 로버트 마틴은 객체지향 설계의 기본 원칙인 SOLID를 제안했습니다.

* SRP (Single Responsibility Principle) : 단일 책임 원칙
* OCP (Open-Closed Principle) : 개방-폐쇄 원칙
* LSP (Liskov Substitution Principle) : 리스코프 치환 원칙
* ISP (Interface Segregation Principle) : 인터페이스 분리 원칙
* DIP (Dependency Inversion Principle) : 의존성 역전 원칙



### SRP (Single Responsibility Principle)

SRP(Single Responsibility Principle)는 클래스나 모듈은 하나의 책임만 가져야 한다는 원칙입니다. 즉, 클래스나 모듈이 변경되어야 하는 이유는 단 하나의 이유여야 한다는 것을 의미합니다. 이 원칙을 따르면 클래스나 모듈의 유지보수성과 재사용성이 높아집니다.

### OCP (Open-Closed Principle)

OCP(Open-Closed Principle)는 소프트웨어 개체는 확장에 열려 있어야 하지만, 변경에는 닫혀 있어야 한다는 원칙입니다. 즉, 새로운 기능을 추가할 때는 기존 코드를 변경하지 않아도 되도록 설계해야 한다는 것을 의미합니다. 이러한 설계를 통해 소프트웨어의 유지보수성과 확장성이 높아집니다.

### LSP (Liskov Substitution Principle)

LSP(Liskov Substitution Principle)는 자식 클래스는 부모 클래스에서 가능한 모든 기능을 사용할 수 있어야 한다는 원칙입니다. 즉, 상속 관계에서 자식 클래스는 부모 클래스의 기능을 제대로 구현해야 하며, 그렇지 않으면 상속 관계가 잘못된 것입니다. 이 원칙을 따르면 소프트웨어의 다형성을 유지할 수 있습니다.

### ISP (Interface Segregation Principle)

ISP(Interface Segregation Principle)는 클라이언트가 자신이 사용하지 않는 메서드에 의존하지 않아야 한다는 원칙입니다. 즉, 인터페이스는 필요한 기능만 제공해야 하며, 사용하지 않는 기능은 제공하지 않아야 한다는 것을 의미합니다. 이 원칙을 따르면 소프트웨어 시스템의 결합도가 낮아지고 유지보수성이 높아집니다.

### DIP (Dependency Inversion Principle)

DIP(Dependency Inversion Principle)는 상위 수준 모듈은 하위 수준 모듈에 의존해서는 안 되며, 추상화된 인터페이스에 의존해야 한다는 원칙입니다. 즉, 모듈 간의 의존 관계를 역전시키고, 추상화된 인터페이스를 통해 결합도를 낮추어야 한다는 것을 의미합니다. 이 원칙을 따르면 유지보수성과 재사용성이 높아집니다.

### 결론

SOLID 원칙은 객체지향 설계의 기본 원칙으로, 객체지향 설계의 품질을 높이기 위해 만들어졌습니다. 이 원칙들을 지키면, 소프트웨어 시스템을 보다 유연하고 확장 가능하게 만들 수 있습니다. 또한, 이러한 원칙을 따르면 코드의 가독성과 유지보수성도 높아집니다. 따라서, 객체지향 개발에서는 SOLID 원칙을 항상 염두에 두고 설계하는 것이 중요합니다.
