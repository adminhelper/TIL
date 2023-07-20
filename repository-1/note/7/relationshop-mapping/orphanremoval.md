# orphanRemoval

### orphanRemoval

JPA에서 엔티티 간 관계를 설정할 때 사용하는 옵션 중 하나입니다. 이 옵션을 사용하면 부모 엔티티와 연관이 끊어진 자식 엔티티들을 자동으로 삭제할 수 있습니다. orphanRemoval 옵션은 CascadeType.REMOVE와 유사하지만, CascadeType.REMOVE는 부모 엔티티가 삭제될 때 자식 엔티티도 함께 삭제되지만, orphanRemoval은 부모-자식 관계가 끊어질 때 자식 엔티티를 삭제합니다.

```java
@Entity
public class Parent {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @OneToMany(mappedBy = "parent", orphanRemoval = true)
    private List<Child> children;
}

@Entity
public class Child {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @ManyToOne
    private Parent parent;

}

```
