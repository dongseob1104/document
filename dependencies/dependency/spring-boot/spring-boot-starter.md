# [spring-boot-starter](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter)

> 자동 구성 지원, 로깅 및 YAML을 포함한 핵심 스타터

---

## 종속성 추가

* Maven

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter</artifactId>
    <version>{version}</version>
</dependency>
```

* Gradle

```Gradle
implementation 'org.springframework.boot:spring-boot-starter:version'
```

---

## 주요 기능

* 자동 구성 지원
  * Spring Boot의 자동 설정(Auto Configuration) 기능을 활용
* 로깅 및 YAML 지원

---

## Starter 종류

|이름      |설명|
|----------|-------------------------------------------------------|
|[spring-boot-starter-cache](./spring-boot-starter-cache.md) | 캐싱 지원을 사용 |
|spring-boot-starter-data-jpa | Hibernate와 함께 Spring Data JPA를 사용 |
|spring-boot-starter-data-jdbc | Spring Data JDBC 사용 |
|spring-boot-starter-jdbc | HikariCP 연결 풀과 함께 JDBC를 사용 |
|spring-boot-starter-security | 인증, 권한 부여 기능 제공 |
|[spring-boot-starter-test](./spring-boot-starter-test.md) | JUnit Jupiter, Hamcrest, Mockito 포함한 라이브러리 사용 |
|spring-boot-starter-thymeleaf | Thymeleaf 뷰를 사용 및 템플릿 엔진 지원 |
|spring-boot-starter-validation | Hibernate Validator, Java Bean Validation 지원 |
|[spring-boot-starter-web](./spring-boot-starter-web.md) | 웹 애플리케이션 개발(Spring MVC + Tomcat) |
|[spring-boot-starter-web-services](./spring-boot-starter-web-services.md) | SOAP 기반의 웹 서비스를 개발 |
|[spring-boot-starter-webflux](./spring-boot-starter-webflux.md) | 리액티브 웹 애플리케이션(Netty) |
|[spring-boot-starter-websocket](./spring-boot-starter-websocket.md) | 웹소켓 빌드 및 지원 |
|[spring-boot-starter-log4j2](./spring-boot-starter-log4j2.md) | Log4j2 기반의 로깅 지원 |
|[spring-boot-starter-logging](./spring-boot-starter-logging.md) | Logback 기반의 로깅 지원 / 기본 로깅 |
|spring-boot-starter-tomcat | Tomcat 사용 / 기본 서블릿 컨테이너 |
|spring-boot-starter-reactor-netty | Reactor Netty 반응형 HTTP 서버 사용 |
|spring-boot-starter-jetty | Jetty 사용 |

---

## 레퍼런스

[Spring Boot Starter로 Spring Boot 애플리케이션 시작하기](https://positive-impactor.tistory.com/117)
[Starters](https://docs.spring.io/spring-boot/reference/using/build-systems.html#using.build-systems.starters)

---

### 🏠 [이동하기](../../../README.md)
