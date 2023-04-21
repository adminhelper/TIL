# @OneToMany와 @JoinColumn

### `OneToMany`&#x20;

어노테이션은 JPA에서 일대다(1:N) 관계를 매핑할 때 사용하는 어노테이션입니다. 일대다 관계는 한 엔티티가 다른 엔티티 여러 개와 관계를 맺는 경우를 의미합니다.

### `@JoinColumn`&#x20;

JPA에서 외래 키(Foreign Key) 컬럼을 지정할 때 사용하는 어노테이션입니다. \
`@JoinColumn` 어노테이션을 사용하여 매핑할 때는 반드시 `@ManyToOne` 어노테이션과 함께 사용해야 합니다.
