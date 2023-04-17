# JPA(Jakarta Persistence API)

## JPA란?

JPA(Jakarta Persistence API)는 객체 관계 매핑(ORM)을 위한 자바 표준 기술입니다. JPA를 사용하면 객체 지향 프로그래밍에서 사용하는 객체와 관계형 데이터베이스에서 사용하는 테이블 사이의 데이터를 매핑(mapping)하여 개발 생산성을 향상시킬 수 있습니다.

### 역사

JPA는 2006년에 최초로 출시되었습니다. JPA는 Java Community Process(JCP)에서 자바 표준 기술로 승인되어, Java EE(Java Enterprise Edition)에서 표준 ORM 기술로 채택되었습니다. 이후 JPA는 Jakarta EE(Java Enterprise Edition)로 이관되면서 이름이 Jakarta Persistence API로 변경되었습니다.

### 장점

* JPA를 사용하면 SQL 쿼리 작성 및 JDBC 코드 작성 등과 같은 반복적이고 지루한 작업을 줄일 수 있습니다.
* JPA는 객체 지향 프로그래밍 언어와 데이터베이스 간의 매핑을 수행하므로, 객체 지향적인 코드 작성이 가능하며, 코드 가독성 및 유지 보수성이 향상됩니다.
* JPA를 사용하면 데이터베이스와의 상호작용이 추상화되므로, 데이터베이스 변경에 대한 영향을 최소화할 수 있다.
* JPA는 일반적으로 데이터베이스 연결과 트랜잭션 관리를 수행하므로, 이러한 작업에 대한 오류를 최소화할 수 있다.

### JPA Entity란?

JPA Entity는 객체 지향 프로그래밍에서 사용되는 클래스를 말합니다. JPA Entity는 데이터베이스의 테이블과 매핑되어, 데이터베이스의 데이터를 객체로 다룰 수 있도록 합니다. JPA Entity는 @Entity 어노테이션으로 표시되며, 클래스 내부에서는 데이터베이스의 컬럼과 매핑되는 필드를 선언합니다. JPA Entity를 이용하면 객체 지향적인 코드를 작성하면서 데이터베이스와의 관계를 관리할 수 있습니다.

### JPA Entity의 장점

JPA Entity의 가장 큰 장점은 객체 지향적인 코드 작성이 가능하다는 것입니다. JPA Entity를 이용하면 데이터베이스의 데이터를 객체로 다룰 수 있으며, 객체 지향 프로그래밍의 장점을 최대한 활용할 수 있습니다. 또한, JPA Entity는 데이터베이스와의 매핑을 어노테이션 기반으로 수행하므로, SQL 쿼리 작성 등과 같은 반복적인 작업을 줄일 수 있습니다. 또한, JPA Entity는 데이터베이스와의 상호작용이 추상화되므로, 데이터베이스 변경에 대한 영향을 최소화할 수 있습니다.

```java
@Entity @Table(name = "person") 
public class Person {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @Column(name = "name")
    private String name;

    @Column(name = "age")
    private int age;

}
// 데이터 저장 
EntityManager entityManager = entityManagerFactory.createEntityManager(); 
EntityTransaction transaction = entityManager.getTransaction();
transaction.begin();
Person person = new Person(); person.setName("John"); 
person.setAge(30);
entityManager.persist(person);
transaction.commit(); entityManager.close();
```

