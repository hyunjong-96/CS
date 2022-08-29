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
    - 특정 기술(hibernate 등..)과 환경에 종속되지 않는 순수한 자바 객체
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
    - Spring MVC의 @Controller, @RequestMapper 등.. 기존 서블릿을 구현할 때 httpservlet을 상속받아 doGet(), doPost()등의 메소드를 구현하고 요청 uri을 매핑하여 비즈니스 로직을 구현해야했지만, Spring MVC에서 제공해주는 어노테이션으로 이러한 과정을 추상화하여 개발자가 비즈니스 로직에 집중할 수 있도록 한다.
    - 마찬가지로 @Transactional도 JDBC를 사용하기 위해서는 connection과 트랜잭션 설정등의 row level의 과정을 거쳐야 했지만 이러한 과정을 추상화하여 개발자가 비즈니스 로직에 집중할 수 있도록 해준다.


</details>

-----------------------

<br>



<br>

-----------------------

### Spring vs Spring Boot

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- spring은 개발에 필요한 의존성 관리를 직접 등록하고 정확한 버전을 명시해주어야했고 war파일로 배포하고 해당 파일을 실행시킬 수 있는 웹 서버나 WAS가 있어야 실행가능하기 때문에 배포 환경에서 톰캣을 깔아줘야한다.
- spring boot는 spring boot starter팩을 통해 개발에 필요한 dependency뿐만 아니라 관련된 의존성도 자동으로 등록해주며 정확한 버전을 명시해주지 않아도 권장 버전으로 자동으로 등록해주어 비즈니스 로직 개발에 집중 할 수 있도록 도와준다.
- 그리고 내장 서블릿 컨테이너 덕분에 jar파일로 간단하게 배포할 수 있게 되었다.
- jar
  - java 애플리케이션을 동작할 수 있도록 자바 프로젝트를 압축한 파일로, JRE만 가지고도 실행이 가능하다.

- war
  - servlet, xml등 servlet context관련 파일로 패키징 된 파일로, 웹 관련 자원만 가지고 있기 때문에 이를 실행하기 위해 tomcat과 같은 웹 서버나, WAS가 필요하다.



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
    - 의존 객체가 존재하지 않아도 객체를 생성할 수 있어 NPE가 발생할 수 있다.

  - @Autowired 주입
    - 필드 이름에 의존관계를 바로 주입하는 방법
    - @Autowired 어노테이션으로 편리하게 주입할 수 있지만, 외부에서 접근이 불가능하기 때문에 테스트시 의존 객체를 수정할 수 없으며, 반드시 DI 프레임워크가 존재해야한다.
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
    - 그 외에 다양한 기능을 제공하기 때문에 BeanFactory를 사용하지 않고 ApplicationContext를 사용한다.
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

  - 구동되는 시점에 Component-Scan을 통해 특정 하위에 있는 Bean으로 등록될 클래스를 모두 스캔하여 Bean으로 등록한다.

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

### Bean LifeCycle

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 빈의 생성부터 소멸 될때까지의 과정
- 스프링 컨테이너 생성 -> 빈 등록 -> 의존관계 주입 -> 초기화 콜백 -> 사용 -> 소멸전 콜백 -> 스프링 종료
- spring은 콜백을 통해 초기화 시점을 알려주는 기능을 제공한다.
  - 초기화 콜백 : 빈이 생성되고 의존관계 주입이 완료된 후 호출
  - 소멸전 콜백 : 빈이 소멸되기 직전에 호출
  - 콜백 방법
    - @PostConstruct : 의존관계 주입 후 호출되는 메소드에 선언
    - @PreDestroy : 빈이 소멸되기 직전에 호출되는 메소드에 선언


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
    - 실행 시점
      - @Before : 대상 메서드 수행 전
      - @After : 대상 메서드 수행 후
      - @After-returning : 대상 메서드 정상 수행 후
      - @After-throwing : 대상 메서드 예외 발생 후
      - @Around : 대상 메서드의 수행 전/후

  - JoinPoint
    - adviced 적용 지점

  - PointCut
    - 복수의 JoinPoint를 하나로 묶은 것

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

<img width="50%" alt="image" src="https://user-images.githubusercontent.com/57162257/184519286-f56aa90e-7f59-47c4-ab89-421813acc157.png">

- WebServer와 WAS (Web Application Server)
  - WebServer : Http 기반으로 동작하며 정적 리소스 (정적  HTML, CSS, 이미지, 영상) 제공
    - NGINX, APACHE
  - WAS : Http 기반으로 동작하며 Web Server 기능을 포함하여 동적 리소스 (동적 HTML, API, Servlet, Spring MVC) 제공
    - Tomcat, Jetty
- Servlet
  - 자바를 이용해서 클라이언트의 요청을 처리하고 결과를 반환하는 자바 웹 프로그래밍 기술
- 동작
  1. 클라이언트의 http 요청이 들어온다.
  2. WAS는 HttpServletRequest, HttpServletResponse 객체를 생성한다.
  3. WAS는 url에 맞는 서블릿을 서블릿 컨테이너에서 찾아 호출한다.
  4. HttpServletRequest로 요청을 처리한다.
  5. HttpServletResponse에 요청 결과를 반환한다.
  6. WAS는 HttpServletResponse를 통해 Http Response Message를 생성 후 클라이언트에게 전달.
- 생명주기
  - 생성 & 초기화
    - 클라이언트 요청이 들어오면 서블릿 컨테이너에 서블릿이 등록되어있는지 확인하고, 등록되어 있지 않다면 서블릿 객체를 생성하고, init() 메서드를 통해 서블릿 컨테이너에 서블릿을 초기화한다.
  - 호출
    - 클라이언트 요청에 따라 service() 메소드를 호출해서 서블릿이 요청을 처리하도록 한다.
  - 종료
    - 컨테이너가 서블릿 종료 요청시 서블릿의 destroy() 메소드가 호출되어 GC에 의해 삭제된다.
  - 생성, 호출, 종료를 구현하기 위해서는 HttpServlet을 상속받아서 구현한다.
- 종류
  - Servlet
    - 서블릿의 필수 메서드를 선언하고 있는 인터페이스
    - 이 표준을 구현해야 서블릿 컨테이너가 해당 서블릿을 실행할 수 있다.
  - GenericServlet
    - Servlet 인터페이스를 상속하여 서블릿 기능을 구현한 클래스
  - HttpServlet
    - GenericServlet을 상속받아 Http 프로토콜을 사용하는 웹 브라우저 기반의 서비스를 제공하는 서블릿을 만들때 상속받아 사용한다.
    - 요청시 service()가 호출되면서 요청 방식에 따라 doGet(), doPost()가 호출된다.

</details>

-----------------------

<br>



<br>

-----------------------

### 일반 클래스와 서블릿 클래스의 차이

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- main() 메서드에서 직접 호출되는 일반 클래스와는 달리 서블릿 클래스는 서블릿 컨테이너가 클래스 로더에 의해 로드하여 호출한다.

</details>

-----------------------

<br>



<br>

-----------------------

### 서블릿 컨테이너

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 서블릿 클래스의 규칙에 맞게 서블릿 객체를 생성,호출,종료하는 생명주기를 관리한다.
- 특징
  - 통신지원
    - <img width="50%" alt="image" src="https://user-images.githubusercontent.com/57162257/184520267-8a98d1ad-b6db-4e7a-93a8-7ad41788275e.png">
    - 실제 WAS를 구현하면 많은 사전 작업을 구현해야한다. 하지만 서블릿 컨테이너에서 이러한 과정을 모두 수행해주고 개발자는 비즈니스 로직에 집중할 수 있다.

  - 멀티 스레딩
    - <img width="60%" alt="image" src="https://user-images.githubusercontent.com/57162257/184520298-d654e921-2b36-43c3-be19-c2fdb1c8f08d.png">
    - 자바 스레드를 이용해서 서블릿을 호출한다.
    - 멀티 스레딩을 통해 다중 요청을 효율적으로 처리할 수 있다.

  - 서블릿 생명주기 관리
  - 선언적 보안 관리
  - JSP
    - Java 언어를 기반으로 하는 Server Side 스크립트 언어
    - HTML 코드에 Java언어를 넣어 동적인 웹 페이지 생성
    - JSP는 내부적으로 Servlet으로 변환되어 실행


</details>

-----------------------

<br>



<br>

-----------------------

### Spring MVC

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- spring에서 Http요청을 처리하기 위한 프레임워크로써 Model, View, Controller의 구성으로 이루어져 있다.

- 역할을 나누어 수행하기 때문에 클래스의 결합도가 낮아진다.

- 구조

  - <img width="771" alt="image" src="https://user-images.githubusercontent.com/57162257/184585914-1efdc7ea-843b-43da-ad6f-f14fcd20fba0.png">
  - Handler Mapping
    - 요청 URL에 맞는 핸들러(컨트롤러)를 찾아서 반환해준다.

  - Handler Adapter
    - Hanlder Mapping에서 찾은 핸들러를 수행해줄 adapter를 찾아서 반환해준다.

  - View Resolver
    - view의 논리주소를 물리주소로 변환한다.
    - 핸들러를 수행하고 받은 ViewAndaModel을 통해 view의 name으로 view를 찾고 model의 데이터를 view에 넣어준다.

- 실행

  Http 요청이 들어온다

  1. Handler Mapping을 통해 요청 url에 맞는 핸들러를 찾아 반환한다.
     - 핸들러를 찾는 getHandler() 호출
  2. Hanlder Mapping에서 찾은 핸들러를 실행시켜줄 어댑터를 Handler Adapter를 통해 어댑터를 찾아 반환한다.
     - 어댑터를 찾는 getHandlerAdapter() 호출
  3. 핸들러 어댑터를 통해 핸들러를 호출하고 요청을 처리한 후 ModelAndView를 반환한다.
     - 핸들러 어댑터의 handle() 호출
  4. ViewResolver를 호출해 ModelAndView에서 view의 name으로 view를 찾고, model의 데이터로 view에 데이터를 넣는다.
     - rest api 서비스는 ViewResolver를 호출하지 않는다.
  5. render를 통해 클라이언트에게 View가 반환된다.

</details>

-----------------------

<br>



<br>

-----------------------

### DispatcherServlet

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 서블릿 기반의 웹 서비스 일 때,  서블릿 컨테이너에서 요청 url에 맞는 url Mapping과 서블릿을 추가해주어야한다. 하지만 FrontController 패턴을 이용해 모든 요청을 하나의 서블릿에서 처리하고 각 요청에 맞는 핸들러에 dispatch해주는 역할을 해주는 것이 DispathcerServlet이다.
- 요청이 들어오면 HttpServlet의 service()가 실행되고 DispatchServlet의 doDispatch()가 호출되어 핸들러를 찾고 어댑터를 찾고 비즈니스 로직이 수행되어 클라이언트에게 결과가 반환된다.
- 상속
  - ![image-20220815152831066](/Users/flab1/Library/Application Support/typora-user-images/image-20220815152831066.png)
  - DispatcherServlet -> FrameworkServlet -> HttpServletBean -> HttpServlet -> GenericServlet -> Servlet을 상속받고 있다.


</details>

-----------------------

<br>



### Handler Mapping과 Handler Adapter의 처리 우선순위

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- Handler Mapping
  0. RequestMapping HandlerMapping
     - @ReqeustMapping 어노테이션을 사용하고 url mapping이 일치하는 핸들러를 찾는다.
  1. BeanNameUrl HandlerMapping
     - 핸들러의 Bean이름과 url을 비교하여 핸들러를 찾는다.
     - 빈 이름에 ANT패턴(*, **, ? 등)을 사용한다.
- Handler Adapter
  0. RequestMapping HandlerAdapter
     - @RequestMapping 어노테이션을 사용하는 클래스, 메소드를 대상으로 지원
  1. HttpRequest HandlerAdapter
     - HttpRequestHandler인터페이스를 상속받는 클래스를 대상으로 지원
  2. SimpleController HandlerAdapter
     - Controller인터페이스를 상속받는 클래스를 대상으로 지원

</details>

-----------------------

<br>



<br>

-----------------------

### Servlet Container & Spring MVC

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- <img width="50%" alt="image" src="https://user-images.githubusercontent.com/57162257/184520419-bb7e72c0-84af-4fcd-8f76-31dfc2a1de5a.png">
- Spring MVC도 서블릿 컨테이너에 의해 관리되는 서블릿

</details>

-----------------------

<br>



<br>

-----------------------

### WAS의 Connector

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- <img width="785" alt="image" src="https://user-images.githubusercontent.com/57162257/184608853-19e188ac-f704-487f-bf5a-1ee312a4575c.png">
- 클라이언트의 요청을 받으면 socket을 받아 HttpServletRequest와 HttpServletResponse를 생성하는 역할.
- BIO Connector와 NIO Connector가 있다.
- 공통적인 역할
  - <img width="767" alt="image" src="https://user-images.githubusercontent.com/57162257/184609233-707a5d49-b555-4e11-8062-7360cf136165.png">
  - EndPoint에서 port listener를 통해 socket connection을 얻는다.
  - Socket connection에서 데이터 패킷을 파싱한다.
  - 파싱한 데이터 패킷을 Adapter에서 HttpServletRequest로 변환하여 서블릿 컨테이너에 보낸다.


</details>

-----------------------

<br>



<br>

-----------------------

### NIO Connector & BIO Connector

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- BIO Connector
  - <img width="761" alt="image" src="https://user-images.githubusercontent.com/57162257/184616009-656241e3-a922-46aa-a751-71808694810e.png">
  - 하나의 요청당 하나의 thread를 할당하여 connection이 종료될때까지 사용하는 Blocking 방식
  - 요청당 하나의 thread가 할당되어 요청과 스레드가 1대1 매칭이 되기 때문에 thread 부족현상이 발생할 수 있다.
  - 구성
    - <img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/184611484-30320797-b417-454f-a6ad-c7dc29cd813b.png">
    - Http11Protocol
      - JIoEndPoint
        - Accepter
          - port listener를 통해 socket을 얻는다.

        - Worker
          - Worker thread pool에서 accepter에거 받은 socket을 처리하기 위해 idle 상태인 worker thread를 꺼내온다.
          - 처리할 worker thread가 없다면 accepter는 block된다

      - Http11ConnectionHandler
        - Http11Processor를 가지고 있다.

    - Mapper
      - http요청에 맞는 서블릿에 바인딩 시켜주는 역할

    - CoyoteAdapter
      - 소켓의 http요청을 HttpServletRequest객체로 변환

  - 처리
    1. Accepter에서 port listener를 통해 소켓을 얻는다.
    2. 소켓에 Worker에서 worker thread를 할당해준다.
    3. worker에서 소켓을 처리하기 위해 Http11ConnectionHandler에서 Htt11Processor를 가져온다.
    4. CoyoteAdapter에서 소켓을 HttpServletRequest로 변환하고 서블릿을 호출한다.

- NIO Connector
  - <img width="736" alt="image" src="https://user-images.githubusercontent.com/57162257/184616040-c3af4798-4554-497e-9234-62ed796d4145.png">
  - BIO Connector와 다르게 Poller라는 특수한 스레드를 사용해서 데이터를 읽을수 있는 상태의 소켓만 worker thread에 할당된다.
  - 요청과 worker thread가 1대1 매칭이 되지 않기 때문에 thread개수보다 더 많은 요청을 받을 수 있다.
  - 구성
    - <img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/184613618-768f017e-c74b-4b26-b1b2-c4aea83d54a4.png">
    - Http11NIO Protocol
      - NIO EndPoint
        - Accepter
          - port listener를 통해 소켓을 얻는다.
          - 소켓(socket connection) -> NIO Channel object -> Poller Event object 로 캡슐화한다.
          - Poller Event를 Poller Event Queue에 저장

        - Poller
          - Poller Event Queue에 저장된 Poller Event를 Nio Channel로 풀어주고 Selector에 Nio Channel을 저장한다.

        - Worker
          - 읽을 수 있는 NIO Channel에 worker thread을 할당한다.
          - NIO Channel의 소켓을 Socket Proccessor로 캡슐화한다.

      - Http11ConnectionHandler
        - Http11Processor

    - Mapper
    - CoyoteAdapter
      - 소켓의 http요청을 HttpServletRequest로 변환하여 서블릿을 호출한다.

  - 처리
    1. Accepter에서 소켓을 얻고 소켓 -> NIO Channel -> Poller Event로 순서대로 캡슐화 한 후 Poller Event Queue에 저장한다.
    2. Poller 스레드가 Poller Event Queue에 저장된 Poller Event를 꺼내서 NIO Channel을 Selector에 저장한다.
    3. 저장된 NIO Channel 중 데이터를 읽을 수 있는 것을 Poller가 NIO Channel에 Worker Thread를 할당한다.
    4. Worker Thread에서 NIO Channel을 Socket Processor로 변경하고 Http11ConnectionHandler에서 Http11Processor를 가져온다.
    5. CoyoteAdapter에서 소켓의 http요청에 대해서 HttpServletRequest을 생성하고 서블릿을 호출한다.


</details>

-----------------------

<br>





<br>

-----------------------

### Servlet 3.0 & Servlet 3.1

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- Servlet 3.0 이전

  - 서블릿 컨테이너에서의 요청과 서블릿에서의 처리가 1대1 매칭이기 때문에 서블릿의 요청이 끝날때까지 요청 스레드가 idle 상태로 유지된다.
  - 스레드 부족현상 발생

- Servlet 3.0 (Async - Blocking)

  - <img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/184616344-ae9e77e2-ef69-4970-b247-f883e2c8c531.png">

  - 비동기 처리를 추가해 서블릿 컨테이너의 요청 스레드와 서블릿의 처리 스레드를 분리하였다.

  - 처리

    1. 서블릿 컨테이너의 요청 스레드가 서블릿 호출시 HttpServletRequest의 startAsnyc()를 호출해 AsyncContext를 선언한다.

    2. AsyncConext를 통해 요청 처리 스레드가 생성되고 요청을 처리한다.
    3. 처리 스레드가 실행되는동안 요청 스레드는 반환되지만 클라이언트와의 요청은 끊어지지 않는다.
    4. 처리 스레드가 완료되면 HttpServletResponse에 결과를 넣고 반환 후 요청 스레드를 종료한다.
    5. 서블릿 컨테이너가 결과를 반환하고 클라이언트와의 요청을 끊는다.

  - 문제점

    - Async Servlet으로 서블릿 컨테이너의 요청 스레드와 서블릿의 처리 스레드는 분리가 되었다. 하지만 처리가 오래걸리는 요청이 들어오면 서블릿 컨테이너와 서블릿 사이의 I/O가 오래걸리게 되고 Block이 발생한다.

- Servlet 3.1 (Asnyc - Non Blocking)

  - 읽는 데이터가 크다면 서블릿에 읽기 위한 대기로 인해 Block이 생기고 쓰는 데이터가 크다면 서블릿 컨테이너에서 쓰기 위한 대기로 Block이 생기게 된다.
  - Read / Write Listener를 통해 3.0의 Blocking 문제를 해결할 수 있다.
  - Read Listener
    - onDataAvailable
      - 컨테이너가 서블릿이 읽을 데이터가 있다면 호출한다.
      - 호출시 ServletInputStream.isReady()가 false로 선언되고 blocking없이 데이터를 읽을 수 있을때 true로 변경한 후 데이터를 읽는다.

    - onAllDataRead
      - 서블릿이 데이터를 blocking없이 읽을 수 있을 때 호출된다.
      - 내부적으로 Writer Listener를 호출.

  - Writer Listener
    - onWritePossible
      - 컨테이너가 쓸 데이터가 있는 즉시 호출한다.
      - 호출 시 ServletOutputStream.isReady()가 false로 선언되고 컨테이너 스레드는 스레드 풀에 반납했다가 blocking없이 데이터를 쓸 수 있을때 true로 변경되면 요청 스레드를 다시 할당 받아 결과를 반환한다.


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

### 적절한 스레드 찾기

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- spring은 멀티 스레드를 사용하기 때문에 스레드의 양에 따라 서버의 효율성에 많은 영향을 미친다. 그렇기 때문에 최적의 스레드를 찾아 서버를 돌려야한다.
- 최대 스레드 수에 따르는 영향
  - 너무 낮게 설정
    - 서버 리소스는 여유롭지만 클라이언트의 응답 지연

  - 너무 높게 설정
    - CPU/ 메모리 과부하로 서버 다운

- 애플리케이션 로직의 복잡도 / CPU / 메모리 / 컨텍스트 스위칭 / 네트워크 속도 등 여러가지 요소가 복합적으로 작용하기 때문에 일반화 할 수 없다.
- 특정 스레드 수를 정하고 성능 테스트 툴을 이용해 물리적으로 적절할 값을 찾아야한다.
  - naver의 nGrinder


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

### Persistence

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 데이터를 생성한 프로그램이 종료되도 데이터는 삭제되지 않는 데이터의 특성
- 메모리상 데이터를 JDBC, PersistencFramework를 통해 데이터베이스에 저장하여 영속성 부여

</details>

-----------------------

<br>



<br>

-----------------------

### Persistence Framework

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 데이터베이스에 연동되는 시스템을 빠르게 개발하고 안정적인 구동을 보장하는 프레임워크
- 종류
  - SQL Mapper
  - ORM


</details>

-----------------------

<br>



<br>

-----------------------

### SQL Mapper & ORM

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- SQL Mapper
  - 객체와 SQL을 매핑시켜주는 기술
  - 장점
    - SQL을 그대로 사용하기 때문에 복잡한 SQL에 강하다.

  - 단점
    - DBMS마다 쿼리가 다르기 때문에 DBMS에 종속적이다.

- ORM (Object Relation Mapping)
  - 객체와 객체형 데이터베으스를 매핑시켜주는 기술
  - 장점
    - SQL이 아닌 쿼리 메소드로 데이터를 조작할수 있기 때문에 객체지향적이고 생산성이 좋다.

  - 단점
    - ORM만으로 복잡한 서비스를 구현하기 어렵다.
    - 잘못된 구현은 속도 저하와 일관성을 무너트릴수 있다.


</details>

-----------------------

<br>



<br>

-----------------------

### JDBC

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 데이터베이스에 접근하기 위해 자바에서 제공하는 API
- 모든 자바의 데이터베이스 접근의 기본
- Plain JDBC
  - JDBC를 통해 데이터베이스에 접근하기 위해서는 `Driver 로드 -> 데이터베이스 연결을 위한 Connection생성 -> Statements를 통한 질의 -> 질의 결과 ResultSet에 저장 -> 생성한 객체 close` 의 과정을 거쳐야한다.


</details>

-----------------------

<br>



<br>

-----------------------

### Spring JDBC

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- <img width="760" alt="image" src="https://user-images.githubusercontent.com/57162257/184825410-56d86328-0d02-4d35-bc52-138100d6315f.png">

- JDBC Template
  - Spring JDBC의 접근 방법 중 하나, Spring JDBC의 데이터베이스 접근을 편리하게 해준다.
  - JDBC Template는 Spring JDBC가 데이터베이스 접근을 할수 있게 JDBC의 과정을 대신 처리해주고 `DataSource 설정, 쿼리 작성, 결과 처리` 만 해주면 된다.
- DataSource
  - 데이터베이스의 connection 정보를 가지고 있다.
  - 빈으로 등록하여 JDBC Template에 정보를 제공한다.
  - Connection Pool에서 Connection을 제공하여 connection 과정을 도와준다.
  - 등록 방법
    1. properties.file 에 connection 정보를 등록한다.
    2. DataSource에 place holder를 통해 properties.file의 정보를 받는다.
    3. Bean으로 등록하여 JDBC Template에 정보를 제공한다.
- JDBC Driver
  - 자바 프로그램의 요청을 데이터베이스가 이해할수 있는 프로토콜로 변경해주는 클라이언트 사이드 어댑터.

</details>

-----------------------

<br>



<br>

-----------------------

### JPA (Java Persistence API)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- <img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/184833025-b9ee3124-262c-42dd-8746-953c06c87465.png">
- 현재 자바의 ORM 표준 기술로 인터페이스의 집합
- 애플리케이션과 JDBC사이에 존재하며 Hibernate로 동작하여 내부 JDBC API를 통해 데이터베이스와 통신한다.
- 특징
  - 데이터 중심적 개발에서 객체지향적 개발
  - 생산성
    - 쿼리 메소드를 통해 SQL을 작성하지 않아 비즈니스 로직에 집중할 수 있다.

  - 유지보수
    - SQL은 엔티티 수정시 쿼리도 수정해야한다. 하지만 JPA는 엔티티를 수정해야할때 엔티티 수정 부분만 수정하면 SQL을 자동으로 생성한다.

  - 성능 최적화 기능
    - 1차캐시
    - 쓰기지연
    - 지연로딩

  - 데이터 접근 추상화와 벤더 독립성
    - DBMS 기술에 종속되지 않는다.

  - 패러다임 불일치 해결
    - 데이터베이스는 데이터 중심 설계, 객체는 객체 중심 설계이기 때문에 데이터베이스는 상속, 연관관계 참조 등의 개념을 이해하지 못한다.
    - 상속
      - JPA는 자식 테이블을 저장하면 자동으로 부모 테이블과 자식 테이블을 저장하는 쿼리를 만들어 주어 저장된다.
    - 연관관계
      - 연관관계를 참조하는 객체를 저장하면 참조를 외래키로 변경하여 저장해준다.
    - 그래프 탐색
      - SQL 조회시 join을 통한 쿼리를 요청하지 않으면 연관관계를 조회할 수 없다.
      - 지연로딩을 통해 연관관계 객체를 참조할 수 있다.
    - 비교
      - 데이터베이스는 PK로 Row를 비교하고 객체는 동일성(==)과 동등성(equals())으로 비교한다.
      - SQL로 같은 조건을 조회하면 동일성을 보장하지 않는다.
      - JPA로 같은 조건을 조회하면 동일성을 보장한다.


</details>

-----------------------

<br>



<br>

-----------------------

### Hibernate

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- JPA의 구현체 중 하나로 Hibernate 내부의 JDBC API를 통해 데이터베이스와 통신한다.
- HQL (Hibernate Query Language)
  - HQL은 SQL과 유사하지만 SQL에서 지원하지 않는 페이지네이션과 같은 고급 기능을 제공한다.
  - HQL은 객체지향으로써 객체지향의 강점을 누릴 수 있다.
  - HQL은 쿼리 결과를 객체로 변환해준다.


</details>

-----------------------

<br>



<br>

-----------------------

### JPQL (Java Persistence Query Language)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- JPA에서 제공하는 쿼리 방법
- 객체지향 쿼리로써 엔티티 객체를 대상으로 쿼리하며 SQL을 추상화 하기 때문에 데이터베이스에 종속되지 않는다.
- `select m from Membe`


</details>

-----------------------

<br>



<br>

-----------------------

### MyBatis

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- <img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/184833188-186c21c2-3343-47f7-9809-c1d6e67b1efa.png">
- 객체와 SQL을 매핑시켜주는 기술
- 쿼리를 그대로 사용할수 있기 때문에 복잡한 쿼리에 강하지만 DBMS에 종속적이다.

</details>

-----------------------

<br>



<br>

-----------------------

### EntityManagerFactory & EntityManager

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- EntityManagerFactory
  - EntityManger를 생성해주는 팩토리
  - 비용이 비싸기 때문에 일반적으로 하나의 EntityManagerFactory를 생성해서 사용한다.
  - 동시성을 보장하기 때문에 동시에 여러 스레드의 접근을 허용한다.

- EntityManger
  - 엔티티를 영속성 컨텍스트에 의해 관리될수 있도록 하는 역할을 한다.
  - 트랜잭션 당 하나의 EntityManger를 생성해서 사용한다.
  - 동시성을 보장하지 않기 때문에 여러 스레드의 접근을 허용하지 않는다.


</details>

-----------------------

<br>



<br>

-----------------------

### Persistence Context

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 엔티티를 영구저장하고 영속 상태의 엔티티를 관리하는 논리적 개념의 환경
- EntityManger 하나 당 하나의 Persistence Context 존재
- 생명주기
  - <img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/184834414-3960dc77-1542-4e78-8877-45a13c6bf8c7.png">
  - 비영속 (new) : 영속성 컨텍스트에 의해 관리받지 못하고 있는 상태
  - 영속 (merged) : 영속성 컨텍스트에 의해 관리받는 상태
  - 준영속 (detached) : 영속상태였다가 영속성 컨텍스트에서 분리된 상태
  - 삭제 (removed) : 영속성 컨텍스트와 데이터베이스에서 삭제된 상태

- 특징
  - 1차 캐시
    -  영속성 컨텍스트에서 영속 상태의 엔티티가 저장되는 공간
    - Map 형태이며 @Id가 key, 인스턴스 주소가 value
    - EntityManager가 엔티티의 조회를 요청할때 1차 캐시에 저장되어있다면 1차 캐시에 저장된 엔티티를 반환하고 저장되어있지 않다면 Select 쿼리를 생성해서 데이터베이스에 요청 후 1차 캐시에 저장하고 반환한다.

  - 쓰기 지연
    - 엔티티의 삽입, 삭제 요청시 Insert, Delete 쿼리가 바로 데이터베이스에 전달되는것이 아니라 쓰기 지연 SQL 저장소에 저장되어있다가 트랜잭션이 commit()되어 flush 발생시 한번에 쿼리를 데이터베이스에 전달한다.
    - flush
      - 영속성 컨텍스트의 엔티티와 데이터베이스의 테이블을 동기화 하는 작업
      - 직접 사용, JPQL사용, 트랜잭션 commit시 자동 실행된다.

  - 지연 로딩
    - 프록시 객체를 사용하여 연관 객체를 실제로 사용하는 시점에 영속성 컨텍스트에 조회를 요청하고 1차캐시에 있다면 저장된 엔티티를, 없다면 Select 쿼리를 생성해서 반환한다.

  - 더티 체킹
    - JPA에서는 update()를 제공하지 않고 영속 상태의 엔티티가 수정되었다면 flush 시점에 스냅샷과 비교하여 update쿼리를 생성하고 쓰기 지연 SQL 저장소에 저장했다가 다른 쿼리와 함께 데이터베이스에 요청된다.
    - 스냅샷
      - 엔티티가 영속성 컨텍스트에 최초로 들어온 시점을 저장해놓은것.
    - JPA 업데이터 전략
      - 일반적으로 JPA의 업데이트 전략은 엔티티의 전체 필드를 수정하는것이다.
      - DynamicUpdate 어노테이션 사용시 수정된 필드에 대한 update 쿼리만 생성된다.
        - 변경된 필드를 찾고 변경된 필드에 대한 쿼리를 따로 생성하기 때문에 성능 문제가 발생한다.
        - 엔티티에 필드가 매우 많고 특정 필드만 자주 수정될때 사용


</details>

-----------------------

<br>



<br>

-----------------------

### Cascade (영속성 전이)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 영속성 전이란, 어떤 엔티티의 영속상태를 변경할때 연관관계의 엔티티도 동일한 영속상태로 변경시켜주는 것
- 종류
  - CascadeType.ALL : 모든 영속상태 변경을 연관 엔티티도 적용받는다.
  - CascadeType.PERSIST : 엔티티가 영속상태로 변경될때 연관 엔티티도 영속상태로 변경된다.
  - CascadeType.MERGE : 엔티티가 준영속에서 영속상태로 변할때 연관 엔티티도 함께 영속상태가 된다.
  - CascadeType.REMOVE : 엔티티가 삭제될때 연관 엔티티도 삭제.
    - 부모 엔티티가 삭제되면 자식 엔티티(주인)도 함께 삭제
    - 영속성 전이를 적용하지 않으면 자식 엔티티부터 차례로 삭제해야한다.

- 고아객체
  - 부모 엔티티와 연관관계가 끊어진 자식 엔티티
  - 부모 엔티티에서 자식 엔티티가 삭제되면 자식 엔티티의 영속 상태가 remove된다.
  - @OneToMany, @OneToOne에서만 사용할 수 있다.

- REMOVE와 Orphan
  - REMOVE는 부모 엔티티가 삭제되었을때 자식 엔티티는 삭제된다. 하지만 부모 엔티티에서 참조 삭제를 해도 자식 엔티티에는 영향을 미치지 않는다.
  - Orpahn은 부모 엔티티가 삭제되면 자식 엔티티도 삭제된다. 부모 엔티티에서 자식 엔티티의 참조를 제거했을때 자식 엔티티는 삭제된다.


</details>

-----------------------

<br>



<br>

-----------------------

### Propagation 전파단계

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 트랜잭션 경계에서 트랜잭션의 유무에 따라 어떻게 동작할지 결정하는 것

- @Transactional을 선언한 클래스, 메소드에 명시하면, 해당 메소드가 호출될 때 지정된 트랜잭션이 수행된다.

- 종류

  | 종류         | 진행중인 트랜잭션 유                     | 진행중인 트랜잭션 무 | 특징                                           |
  | ------------ | ---------------------------------------- | -------------------- | ---------------------------------------------- |
  | REQURED      | 해당 트랜잭션 사용                       | 새로운 트랜잭션 생성 | Default, 예외 발생시 롤백되고, 호출한곳도 롤백 |
  | MANDATORY    | 해당 트랜잭션 사용                       | 예외 발생            |                                                |
  | REQUIRED_NEW | 해당 트랜잭션 보류, 새로운 트랜잭션 생성 | 새로운 트랜잭션 생성 | 두개의 트랜잭션 독립                           |
  | SUPPORTS     | 해당 트랜잭션 사용                       | 트랜잭션 없이 실행   |                                                |
  | NOT_SUPPORT  | 해당 트랜잭션 보류                       | 트랜잭션 없이 진행   |                                                |
  | NEVER        | 예외 발생                                | 트랜잭션 없이 진행   |                                                |
  | NESTED       | 중첩 트랜잭션 생성                       | 새로운 트랜잭션 생성 | Save point 지점까지 롤백가능, oracle에서 가능  |

  

  

</details>

-----------------------

<br>



<br>

-----------------------

### N+1

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- JPQL의 기능적 특성으로 인해 조회 쿼리가 1개가 아닌 연관 엔티티의 개수 N개만큼 조회쿼리가 발생하는 문제
- Fetch.EAGER
  - findById() 쿼리 메소드 사용시 연관 엔티티를 join 하여 조회한다. **(N+1 발생 x)**
  - 그 외의 쿼리 메소드 사용시 연관 엔티티를 따로 조회한다. **(N+1 발생)**

- Fetch.LAZY
  - 모든 쿼리 메소드 사용시 연관 엔티티를 따로 조회한다. **(N+1 발생)**

- N+1 발생 이유
  - 쿼리 메소드 사용시 조회 주체에 대한 select 쿼리가 생성되기 때문에 연관 엔티티 조회를 하기 위한 select 쿼리가 추가 생성되기 때문이다.

- Lazy 로딩에서 findById()시 N+1 발생 이유
  - Lazy로딩시 연관 엔티티는 프록시 객체로 감싸져있기 때문에 연관 엔티티를 조회하기 위한 select 쿼리가 추가 생성되기 때문이다.


</details>

-----------------------

<br>



<br>

-----------------------

### N+1 해결

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- Fetch Join `(inner join)`
  - Fetch Join이란, 조회 주체가 되는 엔티티만 영속성화하는 것이 아닌 연관 엔티티도 조회하여 영속화해주는 JPQL의 특별한 쿼리.
  - JPQL에 fetch join쿼리를 사용한다.
    - @Query("select o from owner o join fetch o.cats")

- EntityGraph `(outer join)`
  - 쿼리 메소드에 @EntityGraph 어노테이션을 사용하여 attributePaths 속성에 연관 엔티티 필드 값을 작성하고 join 없이 JPQL을 작성한다.


</details>

-----------------------

<br>



<br>

-----------------------

### JPQL에서 일반 Join 과 Fetch Join의 차이

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 일반 Join
  - JPQL에 일반 join문을 작성하면 join 쿼리는 발생한다. 하지만 JPQL은 조회 주체 엔티티만 영속화 해주기 때문에 join 대상 엔티티에 대한 영속 관리까지는 관여하지 않는다.
  - 그렇기 때문에 join문을 생성했더라 하더라도 그래프탐색으로 불러오게 되면 LazyInitialization Exception 발생

- Fetch Join
  - 조회 주체 엔티티와 fetch join 대상 엔티티까지 join하여 영속화 해주는 JPQL의 특별한 쿼리


</details>

-----------------------

<br>



<br>

-----------------------

### Fetch join 한계

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- Pagination
  - Fetch join으로 Pagination 요청시 limit 쿼리를 생성하지 않고 memory에 데이터를 불러와 페이징 처리를 하여 OutOfMemory가 발생할 수 있다.
  - 발생 이유
    - Join으로 limit조회시 주최 엔티티의 개수 * 연관 엔티티의 개수만큼의 row가 발생되고 JPA가 원하는대로의 페이징은 SQL에서 처리를 하지 못하여 모든 데이터를 메모리로 불러온다음에 JPA가 메모리에서 페이징을 처리하게 발생하는 것.
  - 해결 방법
    - @BatchSize
      - toMany 연관관계에 @BatchSize어노테이션을 선언한다.
      - 조회 주체에 쿼리에 limit쿼리가 생성되고 조회 주체의 id를 In절에 size만큼 묶어서 연관관계를 조회한다.
      - BatchSize사용시 추가 쿼리 생성은 불가피 하지만 in 쿼리로 모든 연관관계를 불러오는 것보다는 효율적인 성능을 제공해주기 때문에 성능 개선이 도움이 된다.
      - 하지만 BatchSize와 Fetch join을 함께 사용하면 Fetch Join의 우선순위가 높기 때문에 BatchSize가 무시되고 InMemory 이슈가 발생한다.
  
- Miltiple Collection Join
  - 엔티티에 2개 이상의 ToMany 연관관계를 fetch join으로 조회시 `MultipleBagFetch Exception`이 발생한다.
  - 발생 이유
    - 2개 이상의 ToMany 연관관계를 fetch join으로 조회할때 SQL결과에서 ROW의 중복 문제로 인해 매핑을 할 수 없기 때문이다.
  - 해결 방법
    - Set
      - ToMany 연관관계 자료형을 Set으로 선언하면 복잡한 중복문제를 해결해주어 MultipleBagFetch Exception문제를 해결할 수 있다.
      - 하지만 Set자료형도 fetch join으로 Pagination 요청시 In Memory 이슈가 발생한다.
  
    - @BatchSize
      - BatchSize시 MultipleBagFetch Exception을 해결하고 Pagination의 InMemory도 해결할 수 있다.


</details>

-----------------------

<br>



<br>

-----------------------

### BatchSize로 Pagination과 MultipleBagFetchException을 모두 해결할 수 있으니 Fetch Join은 사용하지 않아도 되는가?

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- BatchSize는 N+1문제를 최대한 in 쿼리로 최소한의 성능을 제공하기 때문에 최선의 방법이 아니다.
- ToOne 연관관계에서는 fetch join으로 한번의 쿼리로 처리한다.
- ToMany 연관관계에서는 여러 Collections 중 데이터가 가장 많은 쪽에 Fetch join을 사용하고 나머지는 BatchSize를 통해 성능을 보장한다.

</details>

-----------------------

<br>



<br>

-----------------------

### MultipleBagFetch Exception

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 2개 이상의 List자료형의 연관관계를 fetch join으로 조회하려고 할때 발생하는 이슈
- 2개 이상의 List를 fetch join으로 불러왔을 때 데이터베이스 ROW의 중복 문제로 인해 매핑을 할수 없게 된다.
- Set자료형으로 ROW의 복잡한 중복 문제를 해결하거나 BatchSize를 통해 연관관계를 따로 조회하여 중복 문제를 해결한다.
- <img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/185199179-eb44fad5-659e-4de2-b883-20f14a20a770.png">

</details>

-----------------------

<br>



<br>

-----------------------

### @Transactional

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 데이터베이스와 연결하여 데이터를 다루기 위해 필요한 EntityManger생성이나 commit(), rollback, 예외처리 등의 공통된 작업을 처리해야하기 때문에 AOP 기술로 만들어진 어노테이션
- 매서드에 @Transational을 적용하게 되면 클래스가 빈으로 등록될 때 해당 메소드만 트랜잭션 처리가 되도록 오버라이딩된 프록시 객체가 빈으로 등록된다.
- 클래스에 @Transactional을 적용하게 되면 클래스가 빈으로 등록될 때 전체 메소드가 트랜잭션 처리되도록 오버라이딩 되된 프록시 객체가 빈으로 등록된다.
- 주의사항
  - 프록시 객체가 참조할 타겟 클래스의 메소드의 접근 제어자는 public이어야 한다.
    - 접근 제어자가 private이게 되면 프록시 객체는 타겟 클래스의 메소드를 오버라이딩 할 수 없다.

  - 내부 메소드 호출 시 프록시가 적용되지 않는다.
    - 프록시로 감싸져 있는 클래스 내부에서 내부 함수를 호출시 프록시가 감싸는 클래스의 메소드를 호출하는 것이 아닌 자신(this)에 있는 함수를 직접 호출하는 것이기 때문에 프록시가 적용되지 않는다.
    - 해당 함수를 호출하고 싶다면 프록시를 적용시킨 클래스를 별도로 생성하여 프록시를 적용하여 사용하고 싶은 함수를 구현해준다.


</details>

-----------------------

<br>



<br>

-----------------------

### QueryDsl

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 잘못된 쿼리 작성을 하게 되면 컴파일 시점에 잡아 줄 수 있다.
  - JPA은 기본적으로 JPQL을  string 타입으로 작성하게 된다. 그렇기 때문에 잘못 작성된 쿼리는 런타임때 에러를 발생시킨다.
  - QueryDsl은 정적 타입을 사용하기 때문에 잘못 작성된 쿼리가 있다면 컴파일 시점에서 에러를 발생한다.


</details>

-----------------------

<br>



<br>

-----------------------

### OneToOne 양방향 관계 지연 로딩

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- OneToOne 연관관계에서 주인 엔티티에서 연관 엔티티를 호출시 Lazy 로딩이 작동한다, 하지만 주인이 아닌 엔티티에서 주인 엔티티를 호출시 Lazy 로딩이 작동하지 않는다.
- Lazy로딩은 프록시를 통해 작동하는데 프록시는 null을 감쌀수 없다.
- 그렇기 때문에 주인 엔티티에서는 fk가 있기 때문에 null여부를 확인해서 Lazy로딩이 작동된다. 하지만 주인이 아닌 엔티티는 fk가 존재하지 않기 때문에 주인 엔티티에서 fk의 null여부를 확인해야하기 때문에 주인 엔티티를 조회해야해서 Lazy가 아닌 Eager로딩으로 작동되는것이다.
- ToMany 연관관계에서는 연관관계를 Collections로 관리하기 때문에 null을 갖지 않아 주인이 아닌쪽에서도 Lazy로딩이 가능하다.
- <img width="636" alt="image" src="https://user-images.githubusercontent.com/57162257/185201836-6496c92e-87b8-4a46-928a-ede44ff5e35b.png">

</details>

-----------------------

<br>



<br>

-----------------------

### 상속관계 매핑

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 객체의 상속관계를 데이터베이스에 적용시키기 위한 작업
- 상속 매핑
  - 부모 클래스에 @Inheritence 어노테이션을 선언해 상속관계를 명시한다.
  - 종류
    - Singel Table 전략
      - JPA의 default 상속 매핑 전략
      - 모든 자식 테이블의 데이터를 하나의 테이블에 저장
      - dtype을 통해 자식 클래스를 구분한다.

    - Joined 전략
      - 부모 클래스와 자식 클래스를 join하여 객체를 조합하는 전략
      - 부모 클래스와 자식 클래스가 분리되어 생성되며 부모 클래스와 자식 클래스의 id가 동일하여 PK이자 FK가 된다.
      - @Inheritence(strategy = InheritanceType.JOINED)

- MapperSuperClass
  - 테이블의 상속관계 매핑보다는 공통 데이터가 필요한 경우 사용
  - 부모 클래스를 직접 사용하지 않기 때문에 추상 클래스로 사용하며 Entity가 아니기 때문에 데이터베이스에 생성되지 않는다.
  - <img width="256" alt="image" src="https://user-images.githubusercontent.com/57162257/185202078-12d847d1-eee9-4120-9117-18a598ca8e3f.png">

- 임베디드 타입
  - 공통 속성을 정의한 클래스에 @Embaddable을 선언하고 공통 속성을 사용하는 클래스의 필드에 @Embadded를 선언한다.
  - MapperSuperClass와 마찬가지로 상속관계를 매핑하는 것이 아닌 공통 데이터를 엔티티에 추가한다.
  - 엔티티가 아니기 때문에 데이터베이스에 생성되지 않는다.


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

- 자바 애플리케이션에서 인증, 인가를 처리하고 보호 기능을 제공하는 프레임워크
- spring security 사용시 애플리케이션에 보호 기능을 자체적으로 구현할 필요없고 다양한 기능을 확장할 수 있습니다.
- 인증 프로세스
  - <img width="752" alt="image" src="https://user-images.githubusercontent.com/57162257/186381962-e2e43a71-5d8a-4eab-80e4-7e55bad238ce.png">
    1. Security Filter에서 요청을 가로챈다.
    2. UsernamePasswordAuthenticationFilter를 통해 UsernamePasswrodAuthenticationToken 이라는 인증용 토큰을 생성한다.
    3. AuthenticationManger의 구현체인 ProviderManager에게 UsernamePasswordAuthenticationToken을 전달한다.
    4. ProviderManager는 AuthenticationProvider에게 UsernamePasswordAuthenticationToken을 전달한다.
    5. AuthenticationProvider는 실제 데이터베이스에서 사용자 정보를 가져오는 UserDetailsService에게 사용자 정보를 넘겨준다.
    6. UserDetailsService는 사용자 정보를 데이터베이스에서 찾아 UserDetails로 반환한다.
    7. AuthenticationProvider는 UserDetails로 사용자 정보를 비교한다.
    8. 인증이 완료되면 인증 정보를 담은 Authentication을 반환한다.
       - Authentication은 principle (사용자 식별), cridential (암호), authorities (권한) 으로 구성되어있다.
    9. Authentication을 AuthenticationFilter로 반환하고 SecurityContext에 Authentication을 저장한다.
       - SecurityContext는 세션영역으로써 인증된 Authentication을 SecurityContext에 저장한다는 것은 Spring Security가 세션방식으로 인증 방식을 사용한다는 뜻이다.

- Security Filter
  - <img width="493" alt="image" src="https://user-images.githubusercontent.com/57162257/186384232-91963797-5547-46ee-9c6b-0cec4fdf23b2.png">
  - <img width="500" alt="image" src="https://user-images.githubusercontent.com/57162257/186384310-6ada9459-8671-480c-a25d-ccae60eeb199.png">
  - Security Filter는 서블릿 컨테이너의 Filter와 마찬가지로 DispatcherServlet 요청 전에 사용되는 필터이다. 하지만 Security Filter는 서블릿 컨테이너의 Filter Chain에 DelegatingFilterProxy를 끼워넣고 SecurityFilterChain이 Filter의 역할을 위임하도록 한다.
  - 방법
    - WebSeucrityConfiguerAdapter라는 Filter chain을 구성하는 클래스를 상속받는 Configure클래스를 생성하여 configure() 를 오버라이딩하여 filter chain을 구성할 수 있다.

  - 종류
    - UsernamePasswordFilter : login요청을 감시하며 인증과정 진행.
    - SessionManagementFilter : 요청이 시작된 이후 인증된 사용자인지 확인하고, 인증된 사용자인 경우 동시 로그인 확인 등을 확인한다.
    - ExceptionTranslationFilter : filter chain내에서 발생되는 모든 예외를 처리한다.
      - AuthenticationEntryPoint, AccessDeniedHandler
    - 등 ...


</details>

-----------------------

<br>



<br>

-----------------------

### Spring Security JWT

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- JWT 적용 이유
  - 일반 Spring Security는 저장된 Authentication을 SecurityContext에서 별도의 스레드로 세션이 유지되도록 관리하여 상대적으로 무겁고 유지비용이 발생하게 됩니다.  그렇기 때문에 별도의 유지 비용과 공간이 필요없는 JWT를 사용하여 인증, 인가 처리를 Security에 적용한다.

- 적용 방법
  - JWT 생성, 유효 검사, 인증 처리를 위한 JwtTokenProvider 클래스 구현하였고 이를 사용하기 위해 JwtAuthenticationFilter를 구현하였습니다. 그리고 기존 인증 필터인 UsernamePasswordFilter의 이전에 수행할 수 있도록 security filter chain 설정을 통해 인증 구현.


</details>

-----------------------

<br>



<br>

-----------------------

### Filter 와 Security Filter

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- Filter와 Security Filter는 동일하게 Servlet에 요청되기전에 실행되어 요청 확인 및 가공한다.
- 일반 Filter는 서블릿 컨테이너에 직접 등록하여 사용하는 필터이고 Security Filter는 DelegatingFilterProxy가 서블릿 컨테이너의 Filter에 등록되어 Filter 작업을 Security FilterChain으로 위임하여 실행되는 필터.

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
