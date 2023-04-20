# JdbcTemplate

## JdbcTemplate이란?

JdbcTemplate은 스프링 프레임워크에서 제공하는 데이터베이스 연동을 위한 유틸리티 클래스입니다. JDBC(Java Database Connectivity)를 사용하여 데이터베이스에 접근하고 쿼리를 실행하는 코드를 작성하는 작업을 간소화하여 개발자가 더 쉽게 데이터베이스를 다룰 수 있도록 지원합니다. \
JdbcTemplate은 JDBC API에서 제공하는 모든 기능을 사용할 수 있으며, 예외 처리 및 자원 해제와 같은 부분을 자동으로 처리해주기 때문에 안정적이고 간편한 데이터베이스 연동을 가능하게 합니다.



```java
import org.springframework.jdbc.core.JdbcTemplate; 
import java.util.List;

public class MyDAO {

    private JdbcTemplate jdbcTemplate;

    public void setJdbcTemplate(JdbcTemplate jdbcTemplate) {
        this.jdbcTemplate = jdbcTemplate;
    }

    public List<MyData> getAllData() {
        String sql = "SELECT * FROM my_table";
        return jdbcTemplate.query(sql, new MyDataRowMapper());
    }
    
    private static class MyDataRowMapper implements RowMapper<MyData> {
        public MyData mapRow(ResultSet rs, int rowNum) throws SQLException {
            MyData data = new MyData();
            data.setId(rs.getInt("id"));
            data.setName(rs.getString("name"));
            data.setValue(rs.getDouble("value"));
            return data;
        }
    }
}

```
