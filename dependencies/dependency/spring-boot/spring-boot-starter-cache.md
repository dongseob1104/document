# [spring-boot-starter-cache](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-cache)

> 자주 사용되는 데이터를 임시 저장소(캐시 메모리)에 저장해 빠른 재사용을 가능하게 하는 기능을 제공
>
> Redis 등 캐싱된 데이터를 읽어오기 때문에 실제 DB까지 해당 요청이 전달되지 않아 접근 시간을 절약할 수 있고 DB 부하를 낮출 수 있음

---

## 의존성 추가

* Maven

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-cache</artifactId>
    <version>{version}</version>
</dependency>
```

* Gradle

```Gradle
implementation 'org.springframework.boot:spring-boot-starter-cache:version'
```

---

## 필요한 경우

* 빈번하게 동일한 값이 호출될 때
* 클라이언트에게 전달되는 값이 동일할 때
* 한 번 처리할 때 무거운 리소스를 서버에 요구할 때

## 불필요한한 경우

* 실시간으로 정확성을 요구하는 경우
* 빈번하게 데이터 변경이 일어나는 경우

---

## 레퍼런스

[Spring Boot 에서 Cache 사용하기](https://bcp0109.tistory.com/385)

---

### 🏠 [이동하기](../../../README.md)
