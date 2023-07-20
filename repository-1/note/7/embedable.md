# Embedable

## Embeddable이란?

Embeddable은 객체 지향 프로그래밍에서 사용되는 개념으로, 다른 엔티티와 함께 사용될 수 있는 값 객체를 의미합니다. Embeddable 객체는 일반적으로 별도의 식별자를 가지지 않으며, 소유하는 엔티티와 생명주기를 공유합니다.

Embeddable 객체는 일반적으로 복합적인 값을 표현하는 데 사용됩니다. 예를 들어, 주소 정보를 담고 있는 객체를 Embeddable 객체로 구현할 수 있습니다. 이렇게 구현하면 주소 정보를 포함하는 엔티티에 별도의 주소 정보 필드를 만들지 않아도 됩니다.

JPA에서 Embeddable 객체는 `@Embeddable` 어노테이션을 사용하여 정의합니다. Embeddable 객체를 사용하는 엔티티에서는 해당 필드에 `@Embedded` 어노테이션을 사용하여 Embeddable 객체를 지정합니다.

```java
import javax.persistence.Embeddable;

@Embeddable
public class Address {
    private String street;
    private String city;
    private String state;
    private String zipCode;
}
```

```java
import javax.persistence.Embedded;
import javax.persistence.Entity;
import javax.persistence.GeneratedValue;
import javax.persistence.GenerationType;
import javax.persistence.Id;

@Entity
public class Person {
    @Id
    @GeneratedValue(strategy = GenerationType.AUTO)
    private Long id;
    private String firstName;
    private String lastName;
    @Embedded
    private Address address;
}
```
