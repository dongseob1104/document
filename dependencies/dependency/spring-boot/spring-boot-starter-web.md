# [spring-boot-starter-web](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-web)

> 웹 애플리케이션 개발 시 필요한 라이브러리 제공

---

## 의존성 추가

* Maven

```xml
 <dependency>
   <groupId>org.springframework.boot</groupId>
   <artifactId>spring-boot-starter-web</artifactId>
   <version>{version}</version>
  </dependency>
```

* Gradle

```Gradle
implementation 'org.springframework.boot:spring-boot-starter-web:version'
```

---

## 사용이 필요한 이유

* spring-web - 웹 요청을 처리하기 위한 라이브러리
* spring-webmvc - MVC(Model-View-Controller) 기능을 처리 라이브러리
* spring-boot-starter-tomcat - 톰캣 웹서버 라이브러리
* spring-boot-starter-json - Json 관련 작업을 처리하는 라이브러리

---

## WebFlux vs Spring MVC

|특징      | spring-boot-starter-web (Spring MVC) | [spring-boot-starter-webflux (Spring WebFlux)](./spring-boot-starter-webflux.md)|
|---------|--------------------------------------------|---------------------------------------------|
|처리 방식| 동기 (Blocking) | 비동기 (Non-blocking) |
|멀티스레드| 요청마다 새로운 스레드 생성 | 이벤트 루프 기반 |
|기본 웹 서버| Tomcat, Jetty | Netty, Undertow, Tomcat |
|API 스타일| @RestController 기반 | @RestController + 리액티브 API (Mono, Flux) |
|적합한 경우| 일반적인 웹 애플리케이션 | 높은 동시성을 요구하는 웹 서비스 |

## 레퍼런스

[Spring Boot : 스프링 부트 스타터 웹 개념, 예제, 설명](https://jjeongil.tistory.com/2142)

---

### 🏠 [이동하기](../../../README.md)
