# [disruptor](https://mvnrepository.com/artifact/com.lmax/disruptor)

> 이벤트 처리 동시 프로그래밍 프레임워크

---

## 종속성 추가

* Maven

```xml
  <dependency>
    <groupId>com.lmax</groupId>
    <artifactId>disruptor</artifactId>
    <version>{version}</version>
  </dependency>
```

* Gradle

```Gradle
implementation 'com.lmax:disruptor:version'
```

---

## 주요 기능

* lock-free ring buffer 활용
  * 성능 저하 없이 높은 처리량 제공
* Low Latency (낮은 지연 시간)
  * 마이크로초 단위의 빠른 데이터 처리
* Memory Preallocation
  * GC(Garbage Collection) 영향을 최소화
* 멀티스레드 환경에서 이벤트 처리 최적화

---

## 컴포넌트

* RingBuffer: 원형 버퍼 (데이터 저장 공간)
* Event: 처리할 데이터 객체
* Producer: 데이터를 생성하여 RingBuffer에 추가
* Consumer: RingBuffer에서 데이터를 가져와 처리
* Sequencer: 이벤트 순서 제어

---

## 레퍼런스

[[자바] LMAX Disruptor 이해하기 - 네이버블로그](https://blog.naver.com/tommybee/221729420736)

---

### 🏠 [이동하기](../../../README.md)
