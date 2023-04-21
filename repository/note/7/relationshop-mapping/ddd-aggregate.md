# DDD Aggregate

DDD(Domain-Driven Design)에서 Aggregate는 관련된 개념들을 논리적으로 묶어서 트랜잭션 경계를 만드는 개념입니다. Aggregate는 일종의 데이터 모델링 기법으로, 특정한 업무 개념을 묶고 관리하기 위한 논리적인 단위로 구성됩니다.

Aggregate는 불변성(invariant)을 유지하는 일관성 있는 데이터 집합입니다. 불변성을 유지하는 이유는 Aggregate를 구성하는 엔티티나 값 객체 중 일부만 변경되는 것을 방지하고, 전체 Aggregate가 일관성 있게 유지되도록 하기 위해서입니다. Aggregate는 한 개 이상의 엔티티와 값 객체를 포함하며, Aggregate 루트(Root) 엔티티를 기준으로 참조 관계가 형성됩니다.

Aggregate는 DDD에서 핵심적인 개념 중 하나로, 엔티티를 더 작은 단위로 분해하여 일관성 있는 묶음으로 관리함으로써 시스템의 복잡도를 줄이고 유지보수성을 향상시킬 수 있습니다.

```java
public class Order {
    @Id
    private Long id;
    private LocalDate orderDate;
    private String customerName;
    private List<OrderItem> orderItems;
}

public class OrderItem {
    private Long id;
    private String productName;
    private int quantity;
    private BigDecimal price;
}

```
