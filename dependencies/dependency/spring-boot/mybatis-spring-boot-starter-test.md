# [mybatis-spring-boot-starter-test](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-test)

> 통합 테스트와 단위 테스트에서 MyBatis를 사용할 때 편리하게 설정하도록 지원

---

## 의존성 추가

* Maven

```xml
  <dependency>
   <groupId>org.mybatis.spring.boot</groupId>
   <artifactId>mybatis-spring-boot-starter-test</artifactId>
   <version>{version}</version>
   <scope>test</scope>   
  </dependency>
```

* Gradle

```Gradle
testCompile 'org.mybatis.spring.boot:mybatis-spring-boot-starter-test:version'
```

---

## 주요 기능

* @MybatisTest 제공
  * MyBatis 관련 컴포넌트(@Mapper, SqlSessionFactory, SqlSessionTemplate)만 로드
  * Spring Boot Test와 통합하여 가벼운 테스트 환경 구성
  * DataSource 자동 설정 지원
* 인 메모리 데이터베이스(In-memory DB)와 쉽게 연동 가능
  * 별도 DB 없이 H2, HSQLDB 등 인 메모리 DB 사용 가능
* @Transactional 어노테이션 지원
  * 테스트가 끝나면 자동으로 롤백
* Mock 객체 활용 가능
  * @MockBean을 사용해 Bean에 독립적인 테스트 Mocking 가능

---

## 레퍼런스

[Spring Boot (1) MybatisTest를 통한 Mapper 단위 테스트](https://plz-exception.tistory.com/28)

---

### 🏠 [이동하기](../../../README.md)
