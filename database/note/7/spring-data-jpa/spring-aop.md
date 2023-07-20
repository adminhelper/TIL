# Spring AOP

### Spring AOP란?

AOP(Aspect-Oriented Programming)는 OOP(Object-Oriented Programming)의 한계를 보완하기 위해 등장한 프로그래밍 패러다임으로, 애플리케이션의 횡단 관심사(Cross-cutting Concerns)를 분리하여 모듈화하는 것을 목적으로 합니다.

AOP는 애플리케이션의 주요 로직을 담당하는 핵심 기능과 로깅, 보안, 트랜잭션 처리 등의 부가 기능을 분리하여 관리할 수 있습니다. 이를 위해 AOP는 어떤 코드가 어떤 관심사에 속하는지를 명시하고, 필요한 시점에 관심사를 적용하는 방식을 사용합니다.

### Sprinng AOP 적용방식

AOP를 적용하는 방식은 대체로 프록시 패턴을 이용합니다. 원본 객체 대신 프록시 객체를 생성하여, 필요한 시점에 관심사를 적용하고, 이후에는 원본 객체의 메서드를 호출합니다. 이를 통해 애플리케이션 로직과 관심사가 분리되어 유지보수성과 확장성이 향상됩니다.

### Spring AOP 용어

* Aspect: 애플리케이션에서 횡단 관심사(Cross-cutting Concern)를 분리한 모듈입니다. 메서드 호출, 예외 처리, 보안 등 다양한 관심사를 Aspect로 구현할 수 있습니다.
* Join Point: 어드바이스를 적용할 수 있는 위치입니다. 메서드 호출, 예외 발생, 객체 생성 등 다양한 시점이 있습니다.
* Advice: 특정 Join Point에서 실행될 코드입니다. Before, After, Around 등 다양한 Advice 타입이 있습니다.
* Pointcut: Join Point의 집합입니다. Aspect에서 어떤 Join Point를 사용할 지를 결정합니다.
* Weaving: Aspect를 애플리케이션 코드에 적용하는 과정입니다. 컴파일 타임, 로드 타임, 런타임 등 다양한 시점에서 Aspect를 적용할 수 있습니다.
