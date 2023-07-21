# CascadeType.ALL

### CascadeType.ALL

JPA에서 엔티티 간 연관 관계를 설정할 때 사용하는 옵션 중 하나입니다. 이 옵션을 사용하면 부모 엔티티의 상태가 변경되면 연관된 자식 엔티티들의 상태도 함께 변경할 수 있습니다.

scadeType.ALL 옵션은 총 8가지 Cascade 옵션 중 하나로, 모든 Cascade 옵션을 포함하고 있습니다. 따라서 CascadeType.ALL을 설정하면, 부모 엔티티가 저장, 수정, 삭제되거나 detach될 때 연관된 모든 자식 엔티티도 함께 저장, 수정, 삭제, detach됩니다.

```java
@Entity
public class Parent {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @OneToMany(mappedBy = "parent", cascade = CascadeType.ALL)
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
