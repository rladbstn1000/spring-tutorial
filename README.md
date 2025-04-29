# 🌱 Spring Tutorial 정리

이 저장소는 Spring Framework 학습 과정을 정리한 자료를 담고 있습니다. 기본 개념부터 심화 주제까지 단계적으로 정리했으며, 실습 코드와 함께 제공합니다.

---

## 📌 목차

1. [Spring Tutorial 완료](#1️⃣-spring-tutorial를-완료하자)
2. [Spring이 지원하는 기술 조사](#2️⃣-spring이-지원하는-기술들이ocdi-aop-psa-등을-자유롭게-조사해요)
3. [Spring Bean과 Bean 라이프사이클](#3️⃣-spring-bean-이-무엇이고-bean-의-라이프사이클은-어떻게-되는지-조사해요)
4. [스프링 어노테이션 심층 분석](#4️⃣-스프링-어노테이션을-심층-분석해요)
5. [단위 테스트와 통합 테스트 탐구](#5️⃣-단위-테스트와-통합-테스트-탐구)

---

## 1️⃣ Spring Tutorial를 완료하자!

> 기본적인 Spring 프로젝트 생성부터 간단한 API 개발까지 진행한 과정을 정리합니다.

### ✅ 학습 내용
- Spring Boot 프로젝트 생성 방법
- Controller / Service / Repository 계층 구조
- 간단한 REST API 구현

### 📁 api 성공!
![image](https://github.com/user-attachments/assets/72bce027-ce17-4658-988a-379025360452)


---

## 2️⃣ Spring이 지원하는 기술들(IoC/DI, AOP, PSA 등)을 자유롭게 조사해요

> 스프링이 제공하는 핵심 기술 개념에 대해 정리합니다.

### 🔍 주요 개념
- **IoC / DI**: 객체 제어 반전과 의존성 주입
- **AOP**: 관점 지향 프로그래밍 (예: 로깅, 트랜잭션)
- **PSA**: 추상화된 서비스 접근 방식

### 📚 참고 자료
- [Spring IoC 공식 문서](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans)
- [Spring AOP 공식 문서](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#aop)

---

## 3️⃣ Spring Bean 이 무엇이고, Bean 의 라이프사이클은 어떻게 되는지 조사해요

> Spring Container에서 관리되는 Bean의 개념과 생명주기를 설명합니다.

### 🧬 Bean이란?
- Spring Container에 의해 생성 및 관리되는 객체
- `@Component`, `@Service`, `@Repository`, `@Controller` 등으로 등록

### 🔄 Bean Life Cycle
1. 객체 생성
2. 의존성 주입
3. 초기화 (init-method / `@PostConstruct`)
4. 사용
5. 소멸 (`@PreDestroy` / destroy-method)

---

## 4️⃣ 스프링 어노테이션을 심층 분석해요

> Spring에서 자주 사용되는 어노테이션의 기능과 사용법을 정리합니다.

### 📌 주요 어노테이션
- `@Component`, `@Configuration`, `@Bean`
- `@Autowired`, `@Qualifier`, `@Value`
- `@RequestMapping`, `@GetMapping`, `@PostMapping`
- `@Transactional`, `@Async`, `@Scheduled`

### 📂 예제 코드
```java
@RestController
public class HelloController {
    
    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, Spring!";
    }
}
