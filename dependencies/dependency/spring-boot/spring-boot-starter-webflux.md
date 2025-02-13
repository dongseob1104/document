# [spring-boot-starter-webflux](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-webflux)

> 비동기(Asynchronous), 리액티브(Reactive) 웹 애플리케이션을 개발할 수 있도록 지원

---

## 의존성 추가

* Maven

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-webflux</artifactId>
    <version>{version}</version>
</dependency>
```

* Gradle

```Gradle
implementation 'org.springframework.boot:spring-boot-starter-webflux:version'
```

---

## WebFlux vs Spring MVC

|특징      |[spring-boot-starter-web (Spring MVC)](./spring-boot-starter-web.md)|spring-boot-starter-webflux (Spring WebFlux)|
|---------|--------------------------------------------|---------------------------------------------|
|처리 방식| 동기 (Blocking) | 비동기 (Non-blocking) |
|멀티스레드| 요청마다 새로운 스레드 생성 | 이벤트 루프 기반 |
|기본 웹 서버| Tomcat, Jetty | Netty, Undertow, Tomcat |
|API 스타일| @RestController 기반 | @RestController + 리액티브 API (Mono, Flux) |
|적합한 경우| 일반적인 웹 애플리케이션 | 높은 동시성을 요구하는 웹 서비스 |

---

## 레퍼런스

[Spring Starter Web vs Spring WebFlux](https://happydhkim.tistory.com/entry/Spring-Starter-Web-vs-Spring-WebFlux)

---

### 🏠 [이동하기](../../../README.md)
