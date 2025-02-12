# [spring-boot-starter-test](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-test)

> 스프링 부트에서 애플리케이션 테스트를 할 수 있도록 유틸리티와 애노테이션을 제공
>
> 단위 테스트부터 통합 테스트까지 수행을 할 수 있음

---

## 의존성 추가

* Maven

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-test</artifactId>
    <version>{version}</version>
    <scope>test</scope>
</dependency>
```

* Gradle

```Gradle
testImplementation 'org.springframework.boot:spring-boot-starter-test:version'
```

---

## 제공되는 라이브러리리

> 1. JUnit5: Java 애플리케이션의 단위 테스트를 위한 표준 라이브러리
>
> 2. Spring Test & Spring Boot Test: 스프링 부트 애플리케이션에 대한  유틸리티 및 통합테스트 지원
> 3. AssertJ: 하나의 가정이 올바른지 검사할 수 있도록 도와주는 fluent API 라이브러리
> 4. Hamcrest: Matcher Object 라이브러리로 필터, 검색등을 위해 값을 비교할 때 좀 더 편리하게 사용할 수 있게 해준다.
> 5. Mockito : 자바 모킹 프레임워크 라이브러리로 테스트용 임시객체를 만들어 테스트 고립성을 지켜줄 수 있다.
> 6. JSONassert: JSON의 검증을 위한 라이브러리
> 7. JsonPath: JSON을 XPath방식으로 검사할 수 있게 도와주는 라이브러리

---

## 레퍼런스

[[Spring] 스프링 부트에서 테스트 코드 작성하기](https://bezzang2.tistory.com/139)

---

### 🏠 [이동하기](../../../README.md)
