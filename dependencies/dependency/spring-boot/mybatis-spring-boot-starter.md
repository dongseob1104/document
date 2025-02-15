# [mybatis-spring-boot-starter](https://mvnrepository.com/artifact/org.mybatis.spring.boot/mybatis-spring-boot-starter)

> 스프링 부트 MyBatis 애플리케이션 지원
>
> SQL 기반의 데이터 접근을 보다 쉽게 처리할 수 있도록 Spring Boot 환경에서 최적화

---

## 종속성 추가

* Maven

```xml
  <dependency>
   <groupId>org.mybatis.spring.boot</groupId>
   <artifactId>mybatis-spring-boot-starter</artifactId>
   <version>{version}</version>
  </dependency>
```

* Gradle

```Gradle
implementation 'org.mybatis.spring.boot:mybatis-spring-boot-starter:version'
```

---

## 주요 기능

* MyBatis와 Spring Boot의 통합 지원
  * DataSource 자동 설정, MyBatis 연동
  * SqlSessionFactory, SqlSessionTemplate 자동 생성
* XML, Mybatis의 어노테이션 기반 SQL 지원
  * XML 구문의 Mapper tag, @Mapper 어노테이션 기반의 인터페이스 설계 방식 지원
* Spring @Transactional 어노테이션과 병행 가능
  * 트랜잭션 관리 기능과 MyBatis를 쉽게 결합

---

## 레퍼런스

[MyBatis-Spring-Boot-Starter 사용법](https://kils-log-of-develop.tistory.com/576)

---

### 🏠 [이동하기](../../../README.md)
