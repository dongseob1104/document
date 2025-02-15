# [spring-boot-docker-compose](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-docker-compose)

> Spring boot 사용 시 Docker Compose와 연동해 관리 개발 지원

---

## 종속성 추가

* Maven

```xml
<dependency>
   <groupId>org.springframework.boot</groupId>
   <artifactId>spring-boot-docker-compose</artifactId>
   <version>{version}</version>
   <scope>runtime</scope>
   <optional>true</optional>
</dependency>
```

* Gradle

```Gradle
developmentOnly 'org.springframework.boot:spring-boot-docker-compose:version'
```

---

## 주요 기능

* Docker Compose 서비스 자동 실행
  * 애플리케이션 실행 시 docker-compose.yml을 자동으로 실행
* 쉬운 테스트 환경
  * 통합 테스트 시 필요한 데이터베이스나 외부 서비스를 쉽게 실행
* 자동 인식
  * @ServiceConnection 애노테이션을 사용해 애플리케이션이 Docker Compose의 서비스를 자동으로 인식하도록 설정

---

## 레퍼런스

[Docker Compose Support in Spring Boot 3.1](https://velog.io/@kmss6905/Docker-Compose-Support-in-Spring-Boot-3.1)

---

### 🏠 [이동하기](../../../README.md)
