# JPA Repository와 DDD의 Repository

JPA Repository와 DDD의 Repository는 이름은 비슷하지만 다른 개념입니다.

### JPA Repository

JPA Repository는 스프링 데이터 JPA에서 제공하는 인터페이스입니다. JPA Repository를 사용하면 기본적인 CRUD(Create, Read, Update, Delete) 기능을 구현할 수 있습니다. JPA Repository는 인터페이스로 구현되며, 인터페이스 내부에서 자동으로 메서드 구현을 생성합니다. 또한, JPA Repository는 쿼리 메서드(Query Method)라는 기능을 제공하여, 메서드 이름만으로 쿼리를 생성할 수 있습니다.

```java
public interface UserRepository extends JpaRepository<User, Long> {
    Optional<User> findByUsername(String username);
}
```

### DDD의 Repository

DDD의 Repository는 도메인 주도 설계(Domain-driven Design)에서 사용되는 개념입니다. DDD에서의 Repository는 도메인 객체를 데이터베이스에 저장하고, 조회하며, 삭제하는 역할을 담당합니다. DDD에서의 Repository는 데이터베이스와 직접적인 연관이 있지만, JPA Repository와는 다릅니다.

DDD에서의 Repository는 도메인 모델에서 사용되며, 데이터베이스와의 상호작용을 캡슐화합니다. 즉, 도메인 객체가 데이터베이스에 직접 접근하지 않고, Repository를 통해 간접적으로 접근합니다. 또한, DDD에서의 Repository는 인터페이스로 구현됩니다. 인터페이스를 사용하면 도메인 객체와 Repository 간의 의존성을 낮출 수 있으며, 도메인 객체와 Repository를 분리하여 도메인 모델의 복잡성을 낮출 수 있습니다.

```java
public interface OrderRepository {
    void save(Order order);
    void delete(Order order);
    Optional<Order> findById(Long id);
    List<Order> findByUserId(Long userId);
}
```
