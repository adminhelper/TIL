# Hibernate

## Hibernate란?

자바 기반의 ORM(Object-Relational Mapping) 프레임워크로, 객체와 데이터베이스 간의 매핑을 제공합니다. Hibernate는 JPA(Java Persistence API)의 구현체 중 하나로, JPA의 표준 스펙을 따르며, JPA와 함께 사용할 수 있습니다. \
Hibernate는 XML, 어노테이션 등의 방법으로 객체와 데이터베이스 간의 매핑을 수행할 수 있으며, 데이터베이스와의 상호작용을 추상화하여 데이터베이스 변경에 대한 영향을 최소화할 수 있습니다.

### Hibernate의 역사

Hibernate는 2001년에 Gavin King이 개발한 오픈소스 ORM 프레임워크로, 초기 버전에서는 EJB(Entity JavaBean)와 함께 사용되었습니다. 그러나 Hibernate는 자체적으로 영속성 계층(persistence layer)을 구성할 수 있으며, EJB와의 의존성을 제거하고 단독으로 사용할 수 있게 되었습니다. 현재 Hibernate는 Red Hat에서 개발되고 있으며, Java에서 가장 인기 있는 ORM 프레임워크 중 하나입니다.

### 특징

* Hibernate의 가장 큰 특징은 객체 지향적인 코드 작성이 가능하다는 것입니다.&#x20;
* Hibernate는 객체와 데이터베이스 간의 매핑을 자동으로 수행하므로, SQL 쿼리 작성 등과 같은 반복적인 작업을 줄일 수 있습니다.&#x20;
* Hibernate는 데이터베이스와의 상호작용이 추상화되므로, 데이터베이스 변경에 대한 영향을 최소화할 수 있습니다.&#x20;
* Hibernate는 객체와 데이터베이스 간의 매핑을 XML, 어노테이션 등의 방법으로 지정할 수 있으며, 다양한 데이터베이스와 호환됩니다.

**공부중**

관련 메서드

entityManager&#x20;

entityFactoryManager

트랜잭션

JPQL

#### 의존성 주입방법

```
implementation 'org.hibernate.orm:hibernate-core:6.1.7.Final'
implementation 'org.postgresql:postgresql:42.5.4'
```

