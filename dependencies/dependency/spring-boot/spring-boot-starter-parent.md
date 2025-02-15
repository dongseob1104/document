# [spring-boot-starter-parent](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-parent)

> 부모 POM 종속성 및 플러그인 관리 역할
>
> 버전을 명시하지 않아도 호환되는 버전을 자동으로 가져옴
>
> 빌드와 관련된 플러그인이 자동 적용

---

## 종속성 추가

* Maven

```xml
 <parent>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-parent</artifactId>
   <version>{version}</version>
 </parent>
```

* Gradle

```Gradle
implementation 'org.springframework.boot:spring-boot-starter-parent:version'
```

---

## 주요 기능

* 공통된 종속성(Dependency) 버전 관리
* 기본적인 플러그인 설정 제공
* 전역 속성(Property) 관리 제공
* BOM(Bill of Materials)을 활용해 종속성 버전을 일괄 자동 관리 지원

---

## 레퍼런스

[Spring Boot Starter Parent](https://m.blog.naver.com/sthwin/221262046864)

---

### 🏠 [이동하기](../../../README.md)
