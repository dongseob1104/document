# [spring-boot-starter-log4j2](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-log4j2)

> log4j2 제공
>
> log4j의 업그레이드 버전
>
> 등장 순서 log4j -> logback -> log4j2

---

## 종속성 추가

* Maven

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-log4j2</artifactId>
    <version>{version}</version>
</dependency>
```

```xml
※ 참고 사항
 <dependencyManagement>
  <dependencies>
   <!-- 라이브러리 내에 logback 포함하고 있어 Log4j2 충돌 발생 해결 -->
   <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-logging</artifactId>
    <scope>provided</scope>
   </dependency>
  </dependencies>
 </dependencyManagement>
```

* Gradle

```Gradle
implementation 'org.springframework.boot:spring-boot-starter-log4j2:version'
```

```Gradle
※ 참고 사항

configurations {
    configureEach {
        // spring에서는 기본 값으로 logback 사용하기에 log4j2 사용을 위해 제외 설정을 해야 함
        exclude group: 'org.springframework.boot', module: 'spring-boot-starter-logging'
    }
}
```

---

## 주요 기능

* 비동기 로깅 사용으로 성능 향상
* 로그 필터링 제공
* 플러그인 아키텍처 제공
* 로그 파라미터, 이벤트에 더 많은 메타데이터 제공하고 유연성, 확장성 증대

---

## 레퍼런스

[[Java] Spring Boot Log4j2 이해하기 -1 : 주요 특징, 구성 요소, yml 설정방법](https://adjh54.tistory.com/388)
[[Spring Boot] log4j2 사용하기](https://velog.io/@shinyeji28/Spring-Boot-log4j2-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0)
[Spring Boot 로그(Log) 남기기, log4j2을 사용한 로깅 전략](https://yeo-computerclass.tistory.com/552)
[Log4j2, Slf4j, Log4jdbc 설정 방법](https://velog.io/@deannn/Log4j2-Slf4j-Log4jdbc-%EC%84%A4%EC%A0%95-%EB%B0%A9%EB%B2%95)

---

### 🏠 [이동하기](../../../README.md)
