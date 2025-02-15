# [spring-boot-starter-websocket](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-websocket)

> WebSocket 기반의 양방향 통신 개발 지원

---

## 종속성 추가

* Maven

```xml
  <dependency>
   <groupId>org.springframework.boot</groupId>
   <artifactId>spring-boot-starter-websocket</artifactId>
   <version>{version}</version>
  </dependency>
```

* Gradle

```Gradle
implementation 'org.springframework.boot:spring-boot-starter-websocket:version'
```

---

## 주요 기능

* WebSocket 서버 구현 지원
  * 클라이언트와 서버 간 양방향 통신을 지원
  * 실시간 데이터 전송이 필요한 애플리케이션에서 사용
* STOMP 프로토콜 지원
  * 단순 WebSocket이 아닌 STOMP (Simple Text Oriented Messaging Protocol)를 지원하고 Pub/Sub (발행/구독) 방식을 쉽게 구현
  * 메시지 브로커 (예: RabbitMQ, ActiveMQ)와 통합 가능
* @MessageMapping을 통한 메시지 처리
  * @MessageMapping 애노테이션을 사용해 메시지를 처리
* SockJS 지원
  * SockJS를 통해 WebSocket을 지원하지 않는 환경에서도 HTTP 폴링, AJAX등의 대체 기술을 자동으로 사용해 연결을 유지
* 보안 설정 가능
  * spring-security와 함께 사용해 WebSocket 연결에 대한 인증/인가를 설정

---

## 레퍼런스

[[WebSocket] SpringBoot에서의 WebSocket학습_API가이드 따라하기](https://velog.io/@noljis95/WebSocket-SpringBoot%EC%97%90%EC%84%9C%EC%9D%98-WebSocket%ED%95%99%EC%8A%B5%EC%9E%91%EC%84%B1%EC%A4%91)

---

### 🏠 [이동하기](../../../README.md)
