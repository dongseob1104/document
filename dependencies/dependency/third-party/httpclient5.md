# [httpclient5](https://mvnrepository.com/artifact/org.apache.httpcomponents.client5/httpclient5)

> Apache HTTP 클라이언트 라이브러리
>
> HTTP/1.1, HTTP/2를 지원

---

## 의존성 추가

* Maven

```xml
  <dependency>
    <groupId>org.apache.httpcomponents.client5</groupId>
    <artifactId>httpclient5</artifactId>
    <version>{version}</version>
  </dependency>
```

* Gradle

```Gradle
implementation 'org.apache.httpcomponents.client5:httpclient5:version'
```

---

## 주요 기능

* HTTP 요청, 응답 처리
  * HTTP 메소드 및 요청, 응답 제공
* HTTP/2 지원
  * HTTP/2 프로토콜을 지원
  * 다중 요청, 응답을 단일 연결로 처리해 성능 향상
* Connection Pooling
  * httpclient5는 HTTP 연결 풀링을 지원해 재사용 가능한 커넥션을 효율적인 네트워크 자원으로 관리
  * 높은 트래픽 환경에서 성능을 향상
* 커스터마이징 타임아웃
  * 연결 타임아웃, 읽기 타임아웃 설정 지원
* 보안
  * SSL/TLS 통한 보안 연결을 지원해 HTTPS 요청을 안전하게 처리
* Proxy, 인증 설정
  * HTTP 프록시 서버를 설정 또는 인증을 추가하는 기능 지원
* 플러그인 및 인터셉터
  * 로깅, 보안 검사 작업을 처리할 수 있는 인터셉터 추가 가능

---

## 오류 목록

* java.lang.NoClassDefFoundError: org/apache/hc/client5/http/classic/HttpClient
* java.lang.ClassNotFoundException: org.apache.hc.core5.http.protocol.HttpContext

---

## 레퍼런스

[Spring Boot 3.x 업그레이드 시 Apache HttpClient 의존성 문제](https://velog.io/@chiyongs/Spring-Boot-3.x-%EC%97%85%EA%B7%B8%EB%A0%88%EC%9D%B4%EB%93%9C-%EC%8B%9C-Apache-HttpClient-%EC%9D%98%EC%A1%B4%EC%84%B1-%EB%AC%B8%EC%A0%9C)

---

### 🏠 [이동하기](../../../README.md)
