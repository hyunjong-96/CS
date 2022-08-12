# Spring



<br>

-----------------------

### 프레임워크란

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 개발때 빈번히 사용되는 범용 기능들을 제공해 개발 효율의 향상을 목표로 하는 소프트웨어 환경
- 특징
  - 공통적인 개발 환경
  - 프로그램의 흐름을 개발자가 아닌 프레임워크가 제어함으로써 제어의 역전.

- 종류
  - spring
  - node.js
  - Django


</details>

-----------------------

<br>



<br>

-----------------------

### 프레임워크, 라이브러리, API

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 프레임워크
  - 개발에 필요한 범용 기능을 제공하여 개발 효율의 향상을 목표로 하는 소프트웨어 환경

- 라이브러리
  - 다른 사람이 만들어 놓은 재사용 가능한 코드의 집합

- API (Application Programming Interface)
  - 다른 프로그램이 제공하는 기능을 제어할수 있게 만든 인터페이스
  - ex) 소셜로그인 기능은 구글, 카카오 등의 인증프로그램에서 제공하는 인증 API


<img width="473" alt="image" src="https://user-images.githubusercontent.com/57162257/184122111-5f4e5627-bb6d-4a15-bc5b-84c48165356b.png">

</details>

-----------------------

<br>



<br>

-----------------------

### Spring 이란

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 자바 엔터프라이즈 개발을 위한 오픈 소스 애플리케이션 프레임 워크
- 엔터프라이즈
  - 서버로 기업의 업무를 처리하는것.
  - 핵심 정보를 다루기 때문에 보안, 안정성 필수

- Java EE (Java Enterprise Edition)
  - 개발 및 웹 프로그래밍에 필요한 환경과 기능을 제공 (JSP, Servlet, JDBC 등)

- Java SE (Java Standard Edition)
  - 대중적인 자바 플랫폼
  - 자바의 대부분의 패키지가 포함된 에디션 (java.lang, java.util 등 )

- 특징
  - POJO (Plain Old Java Object)
    - 특정 기술(hibernate 등..)과 환경에 종속되지 않는 순수한 자바 객트
    - 미리 정의된 클래스를 확장, 미리 정의된 인터페이스를 구현을 포함하는 것은 POJO가 아니다.

  - IoC (Inversion Of Control)
    - 객체의 생명주기와 의존성 관리를 컨테이너에서 관리하여 개발자가 아닌 spring에서 객체를 제어한다.
    - 프로그램의 제어를 개발자가 아닌 프레임워크에서 관리하여 제어의 역전이라 한다.

  - DI (Dependency Injection)
    - 의존객체를 내부에서 생성하는 것이 아닌, 컨테이너에서 관리하는 객체를 외부에서 주입하여 결합도가 낮아지고 유연성이 높아진다.

  - AOP (Aspect Oriented Programming)
    - 관점 지향 프로그래밍으로써, 어떤 로직을 핵심적 관점과 부가적 관점으로 나누어 관점을 기준으로 모듈화 하는것.

  - PSA (Portable Service Abstraction)
    - AOP기술로 만들어진 어노테이션을 선언하는 것으로 별도의 코드없이 서비스를 제공하는데, 이렇게 서비스 코드가 숨겨진채로 추상화되어 개발 편의성을 제공해주는것.


</details>

-----------------------

<br>



<br>

-----------------------

### DI (Dependency Injection)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 어떤 객체에서 의존 객체를 내부에서 생성하지 않고 외부에서 주입하는것.
- 장점 (사용 이유)
  - 코드를 단순화 시켜준다.
  - 모듈간의 결합도를 낮춰주고 유연성을 향상킨다.
  - 재사용성을 높여준다.
  - 테스트에 용이하다.

- 조건
  - 주입시키려는 객체가 스프링 IoC 컨테이너에 Bean이라는 객체로 등록되어 있어야한다.
    - 그래야 객체를 외부에서 주입시킬수 있다.

- 주입 방식
  - Constructor 주입
    - 생성자를 통해서 의존 관계를 맺는 방법
    - 의존 객체없이는 인스턴스를 사용할수 없도록 강제성을 두어 NPE과같은 이슈를 예방할 수 있다.
    - 스프링에서 권장하는 방법
    - @RequiredConstructor를 사용해 의존관계를 맺는 객체를 보호함과 동시에 생성자 주입으로 의존관계를 맺을 수 있다.

  - Setter 주입
    - Setter메소드를 통해 의존관계를 맺는 방법
    - 외부에 노출되어 의존관계 변경이 가능해진다.

  - @Autowired 주입
    - 필드 이름에 의존관계를 바로 주입하는 방법
    - @Autowired 어노테이션으로 편리하게 주입할 수 있지만, 변경이 불가능하기 때문에 내부 코드에서 직접 수정해야하는 단점이 있다.
    - 테스트코드, 설정을 목적으로하는 @Configuration 이외의 곳에서는 사용을 지양하는 것이 좋다.


</details>

-----------------------

<br>



<br>

-----------------------

### IoC (Inversion Of Control)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 객체의 생명주기 관리와 의존성 관리를 개발자가 아닌 컨테이너에 넘김으로써 모든 객체에 대한 제어권이 바뀌었다는 것을 말한다.

<img width="40%" alt="image" src="https://user-images.githubusercontent.com/57162257/184129954-9fae26c1-8dbb-48ee-9f44-0f912006d59f.png">

- 종류
  - BeanFactory
    - Bean객체를 생성하고 관리하는 최상위 인터페이스
    - 단순히 컨테이너에서 빈을 생성하고 DI를 처리하는 역할만 한다.
  - ApplicationContext
    - BeanFactory를 상속받은 인터페이스.
    - BeanFactory와 마찬가지로 Bean을 등록하고 DI 기능을 수행한다.
    - 구동되는 시점에 Component-Scan을 통해 특정 하위에 있는 Bean으로 등록될 클래스를 모두 스캔하여 Bean으로 등록한다.
    - @Component 어노테이션을 통해 Bean으로 등록할 수 있고 @Component를 확장한 @Controller, @Service, @Repository 모두 컴포넌트 스캔의 대상이다.
    - @SpringBootApplication에서 ApplicationContext를 생성해준다.

</details>

-----------------------

<br>



<br>

-----------------------

### Bean

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 스프링 IoC 컨테이너에서 관리하는 객체

- 등록방법

  - xml

    - xml 설정파일에 의존관계를 맺을 클래스를 빈으로 등록하고 의존성을 등록할 객체를 프로퍼티로 등록하여 참조하게한다.

    - ```xml
      <?xml version="1.0" encoding="UTF-8"?>
      <beans xmlns="http://www.springframework.org/schema/beans"
             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">
       
          <bean id="bookService"
                class="me.wordbe.springgoahead.BookService">
              <property name="bookRepository" ref="bookRepository" />
          </bean>
       
          <bean id="bookRepository"
                class="me.wordbe.springgoahead.BookRepository" />
       
       
      </beans>
      ```

  - @ComponentScann 과 @Component

    - ApplicationContext는 Component-Scan을 통해 특정 패키지 하위를 스캔하여 @Component가 등록되어있는 클래스를 런타임시 Bean으로 등록한다.
    - @Controller, @Service, @Repository 어노테이션은 내부에 @Component로 선언되어 있어 런타임시 Bean으로 등록된다.

  - Java Config

    - @Configuration을 선언한 클래스의 메소드에 @Bean으로 선언 하여 여러개의 Bean을 관리할 수 있다.
    - 별도의 설정이 없다면 메소드의 이름으로 Bean이 등록된다.

</details>

-----------------------

<br>



<br>

-----------------------

### @Component vs@Bean

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- @Component와 @Bean은 둘다 런타임시 ComponentScan으로 탐색하여 Bean으로 등록하는 것.
- @Bean : 개발자가 컨트롤이 불가능한 외부 라이브러리를 Bean으로 등록하고 싶을때
- @Component : 직접 컨트롤이 가능한 Class를 Bean으로 등록하고 싶을때

</details>

-----------------------

<br>



<br>

-----------------------

### Bean Scope

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- Bean의 사용범위를 말하는 것
- singleton : 빈 스코프의 기본값으로 인스턴스가 단 한번만 생성된다.
  - 필드가 공유되기 때문에 멀티 스레드 환경에서 조심히 사용되야한다.
  - 쓰기보다는 일기 객체에 적합하다.

- prototype 
  - IoC 컨테이너에 빈을 요청할때마다 새로운 인스턴스를 생성한다.
  - 빈 생성, 의존관계 주입, 초기화 까지만 관여하고 이후에는 컨터이너에서 관리하지 않는 스코프

- request : http 요청이 들어오고 나갈때까지 유지

</details>

-----------------------

<br>



<br>

-----------------------

### 싱글톤 vs 스프링 싱글톤

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 싱글톤은 전역 상태로 이용할수 있다는 장점이 있지만 다음과 같은 문제점으로 안티 패턴으로도 불린다

  - ```java
    public class Person {
    
        private static Person instance;
    
        private Person() {
            throw new IllegalStateException("Private Constructor");
        }
    
        public static Person getInstance() {
            if (instance == null) {
                instance = new Person();
            }
            return instance;
        }
    }
    ```

  - Private 생성자를 갖고 있어 상속이 불가능하다.

    - 싱글톤은 자신만이 객체를 생성할 수 있도록 private로 제한한다.

  - 테스트하기 힘들다.

    - 싱글톤은 생성 방식이 제한적이기 때문에 Mock객체로 대처하기 어렵다.

  - 서버 환경에서 싱글톤이 1개만 생성됨을 보장하지 못한다.

    - JVM에 분산돼서 설치되는 경우 독립적으로 객체가 생성되어 1개 이상의 객체가 만들어 질 수 있다.

  - 전역 상태를 만들 수 있기 때문에 바람직 하지 못하다.

    - 객체를 자유롭게 접근하고 수정할수 있는 전역 상태로 만드는 것은 객체지향 프로그래밍에서 권장되지 않는다.

- 스프링에서는 객체의 생성을 스프링에게 위임함으로써 싱글톤 패턴을 자바 언어 레벨에서 직접 구현하기 위한 내용들이 모두 제거되어 싱글톤 단점이 극복된다.

  - ```java
    public class Person {
    
    }
    ```

  - private 생성자가 필요없어 상속이 가능하다.

  - 테스트하기 편리하다

  - 프레임워크를 통해 1개의 객체 생성을 보장받는다

  - 객체지향적으로 개발할 수 있다.


</details>

-----------------------

<br>





<br>

-----------------------

### AOP (Aspect Oriented Programming)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 관점지향 프로그래밍으로써 어떤 로직은 핵심적 관점과 부가적 관점으로 나누어 관점에 따라 모듈화 하는것.
- 여러 객체에서 공통으로 사용하는 기능(흩어진 관심사)을 구분함으로써 재사용성을 높여주는 프로그래밍 기법이다.
- 공통으로 사용되는 기능을 모듈화하는 것을 `크로스 컷팅`이라고도 한다.
- 주요 개념
  - Aspect 
    - 흩어진 관심사를 모듈화 한 것
    - Advice + Pointcut을 모듈화 한 것

  - Target
    - aspect를 적용하는 곳 (클래스, 메서드)

  - Advice
    - 실질적으로 aspect가 어떤 일을 할것인지에 대한 부가기능을 담은 구현체

  - JoinPoint
    - advice가 적용될수 있는 위치

  - PointCut
    - JoinPoint에서 advice가 적용될 위치
    - 종류
      - @Before : 대상 메서드 수행 전
      - @After : 대상 메서드 수행 후
      - @After-returning : 대상 메서드 정상 수행 후
      - @After-throwing : 대상 메서드 예외 발생 후
      - @Around : 대상 메서드의 수행 전/후

- 특징
  - 스프링 빈에만 AOP 적용가능


</details>

-----------------------

<br>



<br>

-----------------------

### 프록시 객체

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 타겟 객체를 감싸서 요청을 대신 받아주는 랩핑 오브젝트.
- 호출자가 타겟 객체를 호출하게 되면 타겟이 아닌 타겟을 감싸고 있는 프록시가 호출되어 타겟 메소드의 선처리, 후처리를 실행시키도록 구성되어있다.
- 어떤 클래스가 AOP의 대상이라면 해당 클래스의 빈이 만들어질 때 AOP가 프록시를 자동으로 만들고 원본 클래스 대신 프록시를 빈으로 등록한다.
- 대표적으로 @Transactional 어노테이션
  - @Transactional 어노테이션이 감싸져있는 클래스를 호출할 때 프록시 객체가 호출되어 commit과 rollback등의 반복되는 기능을 처리해준다.

- 특징
  - private method는 프록시객체에서 타겟 객체의 메소드를 참조할수 없기 때문에 private는 프록시 객체에서 사용할 수 없다.
  - 내부에서 자신의 메소드 호출시 프록시 미 적용
    - 프록시 객체에서 선처리 후 타겟 메소드를 실행하기 때문에 내부에서 타겟 메소드 실행시 프록시가 적용되지 않고 메소드가 실행된다.
    - 해결방법은 실행 할 메소드를 다른 클래스로 빼서 프록시 처리 한 후 타겟 메소드를 호출한다


</details>

-----------------------

<br>



<br>

-----------------------

### Servlet

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 

</details>

-----------------------

<br>



<br>

-----------------------

### MVC 패턴

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 

</details>

-----------------------

<br>



<br>

-----------------------

### DAO vs DTO

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 

</details>

-----------------------

<br>



<br>

-----------------------

### Filter, Interceptor

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

<img width="50%" alt="image" src="https://user-images.githubusercontent.com/57162257/184375555-5ced73be-646b-420f-acf4-4abfa70ba727.png">

- Filter
  - spring context 외부에 존재
  - DispatchServlet 이전에 실행되며, 스프링과 무관하게 지정된 자원에 대해 동작한다.
  - 필터가 동작하도록 지정된 자원 이전에 요청내용을 변경하거나 체크할 수 있으며 자원의 처리가 끝난 후 응답 내용에 대해서 수정할 수 있다.
  - 보안 관련 공통 작업, 이미지/ 데이터 압축 및 문자열 인코딩
  - 메서드
    - init(): 필터 인스턴스 초기화
    - doFilter() : 전/후 처리
    - destroy() : 필터 인스턴스 종료

- Interceptor
  - spring context 내부에 존재
  - DispatcherServlet이 Controller를 호출하기 전,후에 실행.
  - 모든 객체(bean)에 접근이 가능하다.
  - 인증/인가 등의 공통 작업, Controller로 넘겨주는 정보 가공
  - 메서드
    - preHanlder() : controller 메서드가 실행되기 전
    - postHanlder() : controller 메서드 실행 후 view 페이지 렌더링 전
    - afterCompletion() : view페이지 렌더링 후
- 실행 순서
  1. 서버를 실행 시켜 서블릿이 올라오는 동안 init()이 실행되고 그 후, doFilter 실행
  2. 컨트롤러에 들어가기 전에 preHanlder 실행
  3. 컨트롤러 수행 후 postHanlder, after Completion, doFilter 순서대로 실행
  4. 서블릿 종료 시 detroy 실행

</details>

-----------------------

<br>



<br>

-----------------------

### AOP, Interceptor

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- Filter, Interceptor, AOP 는 공통된 기능을 처리하기 위한 기능
- AOP는 Filter와 Interceptor와 다르게 메소드 전,후의 실행 지점이 자유롭게 설정 가능
- AOP의 advice와 Interceptor의 차이는 파라미터
  - advice는 JoinPoint를 파라미터로 받아 호출
  - interceptor는 HttpServletRequest, HttpServletResponse를 파라미터로 사용


</details>

-----------------------

<br>



<br>

-----------------------

### 커넥션 풀

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 

</details>

-----------------------

<br>



<br>

-----------------------

### JPA

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 

</details>

-----------------------

<br>



<br>

-----------------------

### Spring Batch

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 

</details>

-----------------------

<br>



<br>

-----------------------

### Spring Security

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 

</details>

-----------------------

<br>



<br>

-----------------------

### MSA vs Monolithic

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- Monolithic
  - 하나의 프로젝트로 구성되어 있어 단일 패키지로 배포하는 아키텍처
  - 장점
    - 개발 환경이 같이서 복잡하지 않다
    - 배포가 간단하다

  - 단점
    - 서비스가 커짐에 따라 빌드/테스트 시간이 오래 걸림
    - 개발 언어가 종속
    - 하나의 오류가 전체에 영향을 미친다.

- MSA
  - 하나의 큰 어플리케이션을 여러 개의 작은 어플리케이션으로 쪼개어 배포하는 아키텍처
  - 독립적인 기능을 수행하는 작은 단위의 서비스로 나누어 개발
  - 장점
    - 서비스 단위로 개발하기 때문에 해당 부분을 온전히 이해하기 쉽다.
    - 새로 추가되는 부분을 빠르게 수정 및 배포가 가능하다.
    - 해당 기능에 맞는 언어, 기술등을 선택하여 개발할 수 있다.
    - 문제가 생기면 해당 부분에서만 문제가 생긴다.

  - 단점
    - 서비스가 분산되어 관리하기 어렵다
    - 통신오류가 잦을 수 있다.


</details>

-----------------------

<br>



<br>

-----------------------

### DDD (Domain Driven Design)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 도메인을 중심으로 설계해 나가는 것 (도메인 별로 나누어 설계)
- 도메인
  - 실제 세계에 있는 개념을 시스템에 넣는 영역
  - 소프트웨어로 해결하고자 하는 문제의 영역
  - 온라인 공연 예매 시스템을 구현할때 도메인은 공연, 예매가 되고, 하위 도메인은 공연 스케줄, 할인 등...


</details>

-----------------------

<br>





<br>

-----------------------

### 프레임워크

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 

</details>

-----------------------

<br>
