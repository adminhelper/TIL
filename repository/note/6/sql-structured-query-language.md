# SQL(Structured Query Language)

### SQL(Structured Query Language)

SQL(Structured Query Language)은 데이터베이스에서 데이터를 관리하기 위해 사용되는 표준 언어입니다. SQL은 RDBMS(Relational Database Management System)에서 가장 많이 사용되며, 데이터의 삽입, 삭제, 수정, 검색 등의 작업에 사용됩니다.

#### 명령어

1. SELECT: 데이터베이스에서 데이터를 검색하는 명령어입니다.
2. INSERT: 데이터베이스에 새로운 데이터를 삽입하는 명령어입니다.
3. UPDATE: 데이터베이스의 기존 데이터를 수정하는 명령어입니다.
4. DELETE: 데이터베이스에서 데이터를 삭제하는 명령어입니다.
5. CREATE: 데이터베이스의 테이블이나 뷰 등을 생성하는 명령어입니다.
6. DROP: 데이터베이스의 테이블이나 뷰 등을 삭제하는 명령어입니다.
7. ALTER: 데이터베이스의 테이블이나 뷰 등의 구조를 수정하는 명령어입니다.

## JOIN&#x20;

#### INNER JOIN&#x20;

* INNER JOIN은 두 개의 테이블에서 공통된 값을 가진 레코드를 반환합니다. 즉, 두 테이블 간의 교집합을 반환하는 Join입니다.

#### LEFT JOIN

* LEFT JOIN은 첫 번째 테이블을 기준으로 두 번째 테이블을 연결하며, 첫 번째 테이블의 모든 레코드를 반환하고, 두 번째 테이블에서 일치하는 레코드가 없으면 NULL 값을 반환합니다.

#### RIGHT JOIN

* RIGHT JOIN은 LEFT JOIN과 반대로, 두 번째 테이블을 기준으로 첫 번째 테이블을 연결하며, 두 번째 테이블의 모든 레코드를 반환하고, 첫 번째 테이블에서 일치하는 레코드가 없으면 NULL 값을 반환합니다.

#### FULL OUTER JOIN

* FULL OUTER JOIN은 두 개의 테이블에서 일치하는 모든 레코드를 반환합니다. 즉, INNER JOIN과 LEFT JOIN, RIGHT JOIN의 합집합을 반환하는 Join입니다.

#### CROSS JOIN

* CROSS JOIN은 두 개의 테이블에서 가능한 모든 조합을 반환합니다. 즉, 첫 번째 테이블의 각 레코드와 두 번째 테이블의 각 레코드를 모두 조합하여 반환하는 Join입니다.

> SQL은 표준화되어 있기 때문에, 다양한 DBMS에서 사용할 수 있으며, 대부분의 DBMS에서 지원됩니다. SQL을 이용하면, 데이터를 쉽고 빠르게 검색하고 조작할 수 있어서 데이터베이스 관리에 효과적입니다.
