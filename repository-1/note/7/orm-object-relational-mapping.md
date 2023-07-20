# ORM(Object-Relational Mapping)

## ORM이란?

ORM은 객체 관계 매핑(Object-Relational Mapping)의 약자입니다. 객체 지향 프로그래밍에서는 객체를 이용하여 데이터를 관리하고, 관계형 데이터베이스에서는 테이블을 이용하여 데이터를 관리합니다. \
ORM은 이 둘 사이에서 매핑(mapping)을 수행하여 객체 지향 프로그래밍에서 사용하는 객체와 관계형 데이터베이스에서 사용하는 테이블 사이의 데이터를 연결하는 기술입니다.

### 역사

ORM은 1990년대 초반에 최초로 등장하였습니다. 초기 ORM 프레임워크 중 하나인 TopLink는 1993년에 등장하였으며, Java 객체와 Oracle 데이터베이스를 연결하는 데 사용되었습니다. 이후 많은 ORM 프레임워크가 등장하였으며, 현재는 Java에서는 Hibernate, JPA, Spring Data JPA 등의 ORM 프레임워크가 널리 사용되고 있습니다.

### 장점

* ORM은 객체 지향 프로그래밍 언어와 데이터베이스 간의 매핑을 수행하므로, 객체 지향적인 코드 작성이 가능하며, 코드 가독성 및 유지 보수성이 향상됩니다.
* ORM을 사용하면 데이터베이스와의 상호작용이 추상화되므로, 데이터베이스 변경에 대한 영향을 최소화할 수 있다.
* ORM은 일반적으로 데이터베이스 연결과 트랜잭션 관리를 수행하므로, 작업에 대한 오류를 최소화할 수 있다.

```java
import javax.persistence.*;
...
@Entity
public class Employee {
    @Id
    private long id;
    private String firstName;
    private String lastName;
    private Address address;
    private List<Phone> phones;
    private Employee manager;
    private List<Employee> managedEmployees;
    ...
    ...
}

```



