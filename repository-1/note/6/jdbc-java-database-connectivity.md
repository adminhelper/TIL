# JDBC(Java Database Connectivity)

## JDBC

JDBC(Java Database Connectivity)는 자바 언어에서 데이터베이스와 연결하여 데이터베이스를 조작할 수 있는 API(Application Programming Interface)입니다. JDBC는 자바 애플리케이션에서 데이터베이스와 통신할 수 있도록 구현된 API로, 데이터베이스와 통신하는 데 필요한 일련의 클래스와 메소드를 제공합니다.

JDBC API는 다음과 같은 주요 구성 요소로 구성됩니다.

1. DriverManager 클래스 DriverManager 클래스는 JDBC 드라이버를 로드하고 데이터베이스와의 연결을 관리하는 클래스입니다.
2. Connection 인터페이스는 데이터베이스와의 연결을 나타내는 인터페이스로, 데이터베이스와의 트랜잭션을 처리하고 SQL 문을 실행할 수 있습니다.

```java
String url = "jdbc:postgresql://localhost:5432/postgres";

Properties properties = new Properties();
properties.put("user", "postgres");
properties.put("password", "password");

Connection connection = DriverManager.getConnection(url, properties);
```

3. Statement 인터페이스는 SQL 문을 실행하기 위한 인터페이스로, SQL 문을 실행하고 결과를 반환합니다.
4. ResultSet 인터페이스 ResultSet 인터페이스는 데이터베이스에서 쿼리 결과를 저장하는 인터페이스로, SQL 문을 실행한 결과를 저장하고 조회할 수 있습니다.

```java
Statement statement = connection.createStatement();

String query = "SELECT * FROM people";

ResultSet resultSet = statement.executeQuery(query);

while (resultSet.next()) {
	String name = resultSet.getString("name");
	
	System.out.println(name);
} 
```
