# [spring-boot-starter-web-services](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-web-services)

> Simple Object Access Protocol(SOAP) 기반의 웹 서비스를 개발을 지원

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

## 주요 기능

* SOAP 웹 서비스 지원
  * REST API가 아닌 SOAP (Simple Object Access Protocol) 기반의 웹 서비스를 개발할 때 사용
  * spring-ws 라이브러리를 포함, WSDL(웹 서비스 정의 언어) 기반 서비스를 쉽게 구현할 수 있도록 지원
* XML 메시징 처리
  * JAXB, StAX, DOM, SAX 등의 XML 파싱 기술을 지원해 SOAP 메시지를 처리
* 메시지 변환 기능
  * MessageDispatcherServlet을 통해 XML 요청을 자동으로 변환하고, 응답을 생성
* 보안 및 전송 기능
  * WS-Security (메시지 서명, 암호화, 인증 등) 기능을 추가해 보안을 강화
  * HTTPS 및 기타 보안 프로토콜과 통합해 보안성을 증대

---

## 레퍼런스

[Spring Initializr 에서 Spring Web / Spring Web Services 차이](https://jframework.tistory.com/33)

---

### 🏠 [이동하기](../../../README.md)
