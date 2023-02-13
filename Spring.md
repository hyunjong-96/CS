# Spring



<br>

-----------------------

### 프레임워크란

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- 개발의 정형화와 표준화를 제공하고 빈번히 사용되는 범용 기능들을 제공해 개발 효율의 향상을 목표로 하는 소프트웨어 환경
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

- 서드 파티
  - 프로그래밍을 도와주는 제 3자가 만든 코드의 묶음.
    - 라이브러리, 프레임워크, 애플리케이션 등..

- 프레임워크
  - 개발에 필요한 범용 기능과 틀을 제공하여 개발 효율의 향상을 목표로 하는 소프트웨어 환경
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
- 사용 이유
  - 초기 서버사이드를 개발할때 스레드, 소켓등을 개발자들이 직접 관리하였기 때문에 개발자 마다 구현 방법이 달라 협업하는데 어려움이 있었다. 이를 위해 Servlet, JSP를 제공하는 Java Enterprise Edition이 탄생되었다.
    하지만 이를 구현하는 과정에서도 개발자마다 달랐기 때문에 정형화하고 표준화하기를 원했고 이를 위해 만들어 진 것이 프레임워크이다.
  - 즉, 스프링은 자바 엔터프라이즈 개발을 위해 정형화되고 표준화된 환경을 제공하고 범용적으로 사용하는 기능을 제공하는 프레임워크이다.
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
    - 어노테이션과 같이 추상화 계층을 사용하여 어떤 기술을 내부에 숨기고 개발자에게 편의성을 제공해주는 것은 서비스 추상화(Service Abstraction)
    - 환경 변화에 상관없이 일관된 방법으로 접근 환경을 제공하는 서비스 추상화 (Portable Service Abstraction)
    - Spring MVC의 @Controller, @RequestMapper 등.. 기존 서블릿을 구현할 때 httpservlet을 상속받아 doGet(), doPost()등의 메소드를 구현하고 요청 uri을 매핑하여 비즈니스 로직을 구현해야했지만, Spring MVC에서 제공해주는 어노테이션으로 이러한 과정을 추상화하여 개발자가 비즈니스 로직에 집중할 수 있도록 한다.
      또한 spring mvc코드를 두고 webflux의존성을 받도록 바꿔주기만 해도 tomcat이 아닌 netty기반으로 실행하게 할 수 있다.
    - 마찬가지로 @Transactional도 데이터베이스를 사용하기 위해서는 connection이 필요한데, JDBC는 직접적으로 connection을 관리하지만, JPA는 EntityManager를 통해 간접적으로 관리하기 때문에 사용 기술에 따라 다르게 사용해야한다. 하지만 TransactionManager 추상화 계층에 의존함으로써 다른 기술을 사용해도 일관성있게 트랜잭션을 사용할 수 있고 트랜잭션 설정등의 row level의 과정을 거쳐야 했지만 이러한 과정을 추상화하여 개발자가 비즈니스 로직에 집중할 수 있도록 해준다.
      - <img width="400" alt="image" src="https://user-images.githubusercontent.com/57162257/196101889-082e7169-856b-4136-b5a5-fab95778ab14.png">


</details>

-----------------------

<br>



<br>

-----------------------

### POJO (Plain Old Java Object)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

- 특정 기술에 종속되지 않고 객체지향의 장점을 유지하는 순수한 형태의 자바
- 특정 기술에 종속되게 된다면 가독성이 떨어져 유지보수에 어려움이 생기고 의존하게 된 자바코드는 확장성이 떨어져 객체지향성을 잃을 수 있다.
- **객체지향적인 원리에 충실하면서, 환경과 기술에 종속되지 않아 상황에 따라 재활용 될수 있도록 설계된 오브젝트.**
- 장점
  - 기술이나 환경에 자유로워 변경에 취약하지 않다.
  - 재사용이 가능하고 확장가능한 객체 지향적 설계 가능.

- Hibernate와 스프링이 대표적인 POJO 프레임워크
  - POJO 프레임워크 : POJO를 이용하면서 엔터프라이즈 서비스와 기술을 그대로 사용할 수 있도록 도와주는 프레임워크

  - Hibernate
    - Persistence기술과 object-RDB 매핑을 순수한 POJO를 이용해 사용할 수 있게 만드는 POJO기반의 persistence 프레임워크
    - JDBC API를 직접사용하게 되면 의존하고 가독성 낮은 자바 코드를 작성하게 된다. Hibernate를 통해 객체지향적인 설계와 구현이 가능하다.
    - JDBC에 종속한 Hibernate는 POJO가 아닌데 어떻게 스프링에서 사용할수 있는가?
      - JPA라는 표준 인터페이스를 정해두었고, 여러 ORM프레임워크들이 표준 인터페이스 아래 구현되어 실행되기 때문에 JPA를 사용하게 된다면 특정 기술에 종속하지 않고 POJO를 이용해 기술을 사용할 수 있게 된다.

  - Spring
    - 엔터프라이즈 서비스들을 POJO기반으로 만든 비즈니스 오브젝트에서 사용할 수 있게 해준다
    - 특정 인터페이스를 구현하거나 상속할 필요없이 라이브러리를 지원한다.
    - AOP기술을 적용해서 객체지향적으로 코드를 작성할 수 있다.
      - 부가기능들을 모듈화하기 때문에 가독성이 좋아지고 핵심기능을 설계하고 구현할때 객체지향적인 가치를 지킬 수 있다.




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

- Spring

  - 개발에 필요한 dependency를 명확한 버전을 명시하고 등록하야한다.

  - 프로그래밍에 필요한 설정을 하나하나 설정해주어야한다.

  - war파일을 실행시켜줄 웹서버가 별도로 설치하여 배포해야한다.

- Spring Boot
  - 개발에 필요한 dependency의 버전을 명시하지 않아도 자동으로 설정하여 등록해주고 starter팩을 통해 설치한 dependency와 관련된 다른 dependency를 한번에 등록시켜준다.
  - AutoConfiguration을 통해 자동으로 개발에 필요한 내부 dependency를 등록하고 관리해준다.
  - jar파일 내부에 tomcat이 포함되어있어 파일 자체로 배포가 가능하다.
  - 이를 통해 비즈니스 로직에 집중하고 실행만 하면 된다.

- jar
  - java 애플리케이션을 동작할 수 있도록 자바 프로젝트를 압축한 파일로, JRE만 가지고도 실행이 가능하다.
- war
  - servlet, xml, JSP등 servlet context(웹 애플리케이션)관련 파일로 패키징 된 파일로, 웹 관련 자원만 가지고 있기 때문에 이를 실행하기 위해 tomcat과 같은 웹 서버(WEB)나, 웹 컨테이너(WAS)가 필요하다.
    - XML
      - HTML과 유사한 마크업 언어
      - 데이터를 보여주는 것이 목적이 아닌, 데이터를 전달하고 저장하는것이 목적
      - 데이터의 무결성을 검증할 수 있다.
      - 계층적 데이터 구조를 가진다
    - JSON
      - 브라우저 통신을 위한 key-value로 이루어진 데이터 포멧
      - XML에 비해 빠른 처리속도
      - 모든 브라우저에서 사용가능
      - 계층적 데이터 구조를 가진다.



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
  - <img width="600" alt="image" src="https://user-images.githubusercontent.com/57162257/192211595-533f3050-518b-475b-ae22-483824a20c1f.png">
  - Aspect 
    - 흩어진 관심사를 모듈화 한 것
    - Advice + Pointcut을 모듈화 한 것
  - Target
    - 어떤 대상에 부가적 기능을 부여할것인지 (클래스, 메서드)
  - Advice
    - 부가기능의 구현체 & 부가 기능의 실행지점
    - 실행 시점
      - @Before : 대상 메서드 수행 전
      - @After : 대상 메서드 수행 후
      - @After-returning : 대상 메서드 정상 수행 후
      - @After-throwing : 대상 메서드 예외 발생 후
      - @Around : 대상 메서드의 수행 전/후
  - JoinPoint
    - 어디에 적용될것인가? (메서드, 클래스, 객체, 필드)
    - Aspect와 같은 aop에서는 메서드, 클래스, 객체, 필드에 AOP를 적용할 수 있다.
      - Aspect : Java에서 제공하는 aop 라이브러리
    - Spring AOP에서는 method 실행 시점에만 adivce가 적용된다.
  - PointCut
    - 실제 advice가 적용될 시점.
  
- 특징
  - 스프링 빈에만 AOP 적용가능
- AOP 적용방법
  - 컴파일
    - .java 파일에서 .class 바이트코드로 컴파일 될때 부가 기능을 적용

  - 클래스 로드
    - .class 바이트코드가 JVM으로 로드될떄 부가 기능을 적용

  - 프록시
    - Spring AOP에서 지원하는 적용방법으로 AOP가 적용된 메소드를 호출할 때 프록시 객체로 감싸서 해당 메소드가 호출될때 부가 기능을 수행하고 타겟 메소드를 호출하게 된다.
    - AOP는 JDK Dynamic Porxy사용



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
- 장점
  - OCP : 기존코드를 변경하지 않고 새로운 기능 추가 가능
  - SRP : 기본 코드가 가지고 있는 역할을 유지지

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

### Dynamic Proxy vs CGLib Proxy

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- 수동으로 프록시 패턴을 구현하게 된다면 인터페이스(DiscountService)와 구현체 객체(RateDiscountService)를 구현하게 된다. 그리고 프록시 패턴을 위해 프록시 객체(RateDiscountServiceProxy)는 인터페이스(DiscountService)를 상속받고 구현체를 사용하여 구현하게 된다.
  하지만 이런 구현은 2개의 빈이 등록되게 된다(RateDiscountService, RateDiscountServiceProxy)

  - <img width="700" alt="image" src="https://user-images.githubusercontent.com/57162257/192232905-5d985e94-0271-41eb-9ee4-f352a2fcf3c2.png">
  - <img width="700" alt="image" src="https://user-images.githubusercontent.com/57162257/192232973-dedc7266-dd7e-4b1a-ab44-4d8e17d3f1da.png">

- Dynamic Proxy

  - ~~Spring은 자동 프록시 팩토리를 통해 직접 프록시 객체를 생성하는데, 프록시를 구현한 객체는 실제 구현체 빈을 프록시 객체가 감싸 빈으로 등록되기 때문에 1개의 빈만 등록되게 된다. (RateDiscountServiceProxy)~~
  - <img width="700" alt="image" src="https://user-images.githubusercontent.com/57162257/192234376-309d4ebe-6c3b-456a-b05c-e29c45c1ce18.png">
  - ~~하지만 다른 곳에서 구현 클래스를 의존하게 된다면 빈으로 등록되어있지않아 에러를 발생시킨다. 또한 Dynamic Proxy는 인터페이스 기반으로 프록시 객체를 생성하게 되는데, 인터페이스를 구현한 클래스가 없다면 프록시객체를 생성할 수 없다.~~
  - <img width="700" alt="image" src="https://user-images.githubusercontent.com/57162257/192236404-fe90cd6a-0d61-40f3-86b4-63dfc17252ba.png">
  - 프록시 팩토리에 의해 런타임시 동적으로 만들어지는 오브젝트
  - 프록시 팩토리에게 인터페이스를 전달하게 되면, Reflection을 통해 인터페이스를 기반으로 프록시 객체를 생성한다.
    - 부가 기능 직접 구현시 InvocationHandler를 상속하여 invoke메서드를 오버라이드 하여 부가 기능을 적용해주어야한다.
  - 한계점
    - 프록시 객체를 실행하기 위해서는 반드시 인터페이스를 생성해야한다. (번거로움)
    - 구현 클래스를 빈으로 등록할 수 없지만, 프록시 객체에서 사용하기 위해 구현 클래스를 생성해야한다. (번거로움)
    - 인터페이스를 상속받고 Reflection API를 통해 프록시 객체를 생성하다보니 성능이 떨어진다.

- CGLib Proxy

  - Dynamic Proxy의 문제를 해결하기 위해 Spring은 CGLib이라는 바이트 조작 라이브러리를 사용하여  프록시 객체가 인터페이스(DiscountService)에 기반하지 않고 클래스(RateDiscountService) 상속을 기반으로 프록시 객체를 생성하게 하였다.
    - 부가 기능 직접 구현시 MethodInterceptor를 상속한 클래스에 interceptor를 오버라이딩하여 부가 기능을 적용해주어야한다.
    - 또한 Enhancer라는 라이브러리를 의존받아 프록시객체를 생성해주어야한다.
  - 구현체를 직접 상속받음으로써 프록시 객체에서 사용할 메서드를 오버라이드 함으로써 성능적으로 향상
    - 타겟 클래스를 처음 호출했을때 CGLib라이브러리를 사용하여 바이트 조작 코드를 생성하고 그 이후에 사용시에는 캐싱된 바이트 조작된 코드를 재사용하기 때문에 성능 향상
  - spring에서는 CGLib Proxy를 사용하지 않았던 이유
    - spring에서 지원하지 않는 방법이였기때문에 별도의 의존성을 추가해야했다(Enhance)
    - default 클래스가 필수적이였다
    - 타겟 클래스의 생성자가 두번 호출
  - spring 3.2부터 spring core에 의존성이 포함되었고 4.0, 4.3에서 이러한 문제를 해결하면서 CGLib이 안정화 되었다.

- @EnableAspectJAutoProxy

  - true :  GCLib Proxy사용
  - false : Dynamic Proxy사용

  

  

  

  

  

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
    - 클라이언트 요청이 들어오면 서블릿 컨테이너에 서블릿이 등록되어있는지 확인하고, 등록되어 있지 않다면 서블릿 클래스를 로딩하고 서블릿 객체를 생성하고, init() 메서드를 통해 서블릿 컨테이너에 서블릿을 초기화한다.
    - 서블릿 생성 및 초기화는 많은 비용이 들기 때문에 한번 생성된 서블릿은 유지한다.
  - 호출
    - 클라이언트 요청에 따라 service() 메소드를 호출해서 서블릿이 요청을 처리하도록 한다.
  - 종료
    - 컨테이너가 서블릿 종료 요청시 서블릿의 destroy() 메소드가 호출되어 GC에 의해 삭제된다.
  - 생성, 호출, 종료를 구현하기 위해서는 HttpServlet을 상속받아서 구현한다.
- 종류
  - Servlet
    - 서블릿의 필수 메서드를 선언하고 있는 인터페이스
    - 이 표준을 구현해야 서블릿 컨테이너가 해당 서블릿을 실행할 수 있다.
    - init(), service(), destroy() 메서드 등이 선언되어있다.
  - GenericServlet
    - Servlet 인터페이스를 상속하여 서블릿 기능을 구현한 클래스
  - HttpServlet
    - GenericServlet을 상속받아 Http 프로토콜 기반의 요청을 처리하는 서블릿을 만들때 상속받아 사용한다.
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
    - 핸들러를 수행하고 받은 ModelAndView을 통해 view의 name으로 view를 찾고 model의 데이터를 view에 넣어준다.

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

- 서블릿 기반의 웹 서비스 일 때,  서블릿 컨테이너에서 요청 url에 맞는 서블릿을 추가해주어야한다. 하지만 FrontController 패턴을 이용해 모든 요청을 하나의 서블릿에서 처리하고 각 요청 url에 맞는 핸들러에 dispatch해주는 역할을 해주는 것이 DispathcerServlet이다.
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
  1. HttpRequestHandler HandlerAdapter
     - HttpRequestHandler인터페이스를 구현하는 클래스를 대상으로 지원
  2. SimpleController HandlerAdapter
     - Controller인터페이스를 구현하는 클래스를 대상으로 지원

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
        - Http11Processor
          - 요청을 Http 정보를 모아 캡슐화
      
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
          - 요청의 http정보를 캡슐화
      
    - Mapper
    - CoyoteAdapter
      - 소켓의 http요청을 ServletRequest(Request)로 변환하여 서블릿을 호출한다.
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

  - 서블릿 컨테이너에서의 요청 스레드(servlet thread)와 서블릿에서의 처리(worker thread)가 1대1 매칭이기 때문에 서블릿의 요청이 끝날때까지 요청 스레드가 idle 상태로 유지된다.
  - 스레드 부족현상 발생

- Servlet 3.0 (Async)

  - <img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/184616344-ae9e77e2-ef69-4970-b247-f883e2c8c531.png">

  - 비동기 처리를 추가해 서블릿 컨테이너의 요청 스레드와 서블릿의 처리 스레드를 비동기 처리로 분리하였다.

  - 처리

    1. 서블릿 컨테이너의 요청 스레드가 서블릿 호출시 HttpServletRequest의 startAsnyc()를 호출해 AsyncContext를 선언한다.

    2. AsyncConext를 통해 요청 처리 스레드가 생성되고 요청을 처리한다.
    3. 처리 스레드가 실행되는동안 요청 스레드는 반환되지만 클라이언트와의 요청은 끊어지지 않는다.
    4. 처리 스레드가 완료되면 HttpServletResponse에 결과를 넣고 반환 후 요청 스레드를 종료한다.
    5. 서블릿 컨테이너가 결과를 반환하고 클라이언트와의 요청을 끊는다.

  - 문제점

    - Async Servlet으로 서블릿 컨테이너의 요청 스레드와 서블릿의 처리 스레드는 분리가 되었다. 하지만 서블릿은 여전히 Blocking I/O였기 때문에 처리가 오래걸리는 요청이 들어오면 서블릿 컨테이너와 서블릿 사이의 I/O가 오래걸리게 되고 Block이 발생한다.
    - 스레드 block이 발생하게되면 스레드는 wait상태로 변경되어 context switching이 발생하고 I/O완료시 running상태로 변경되면서 다시 context switching이 발생하여 총 2번의 context switching발생으로 CPU에 부하를 줄 수 있다.

- Servlet 3.1 (Asnyc, Non Blocking I/O)

  - 데이터가 크다면 서블릿에 읽기 위한 대기로 인해 Block이 생기고 쓰는 데이터가 크 다면 서블릿 컨테이너에서 쓰기 위한 대기로 Block이 생기게 된다.
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

### 비동기

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- @Async

  - Spring에서 스레드 풀을 이용해 비동기 작업을 지원해주는 방법
  - @EnableAsync가 설정되어있어야 효과가 발생한다.
  - 내부적으로 ThreadPoolTaskExecutor의 스레드를 할당받아 비동기 작업을 수행
    - @Async가 ThreadPoolTaskExecutor를 별도로 명시하지 않으면 SimpleAsycnTaskExecutor에서 스레드를 할당받아오는데, 해당 TaskExecutor는 요청마다 스레드를 생성하기 때문에 지양한다.
    - 사용자 지정 ThreadPoolTaskExecutor를 선언하고 사용할 TaskExecutor를 명시한다면 , 해당 ThreadPoolTaskExecutor에서 스레드를 할당받아 비동기 작업을 수행한다.
    - 사용자 지정 TaskExecutor를 선언했다면 별다로 명시하지 않아도 TaskExecutor타입의 빈을 찾아서 자동으로 스레드를 할당시켜준다.

  - 사용자 지정 ThreadPoolTaskExecutor를 빈으로 등록시켜주어야 @Async에서 스레드를 할당받을 수 있다.
    - ThreadPoolTaskExecutor
      - corePoolSize : 풀의 기본사이즈 (1)
      - queueCapacity :  대기 상태의 task를 저장하는 큐 (Integer.MAX_VALUE)
      - maxPoolSize : 풀의 최대사이즈 (Integer.MAX_VALUE)
      - keepAliveSeconds :  corePoolSize를 넘거나 allowCoreThreadTimeout이 ture로 설정되어있다면, corePoolSize가 넘는 스레드는 설정한 시간이 넘게되면 삭제된다.
      - allowCoreThreadTimeout : corePoolSize의 스레드도 삭제된다.

- Thread의 종료 처리

  - JVM은 자식 스레드가 실행되고 있거나 종료되지 않는다면, JVM을 종료할 수 없다.

  - ExecutorService 사용시

    - shutdown() : 새로 실행되는 task를 막는다. (실행중이던 task가 완료되면 종료)
    - shutdownNow() : 현재 실행중인 task를 종료한다. (온전히 종료 작업이 수행되지 않을수도 있다.)
    - awaitTermination() : 설정한 시간만큼 실행중인 task가 완료되길 기다리고, 설정한 시간이 넘어가게 되면 강제종료

  - ThreadPoolTaskExecutor 사용시 (=@Async)

    - keepAliveSeconds, allowCoreThreadTimeout을 설정하여 스레드가 안전하게 종료되도록한다.
    - 빈의 초기화와 삭제 등을 정의하고 있는 DisposableBean인터페이스를 구현한 ExecutorConfigurationSupport클래스를 상속받고 있기 때문에, 애플리케이션 종료시 ExecutorConfigurationSupport.destroy()가 실행되어 실행중인 task를 안전하게 종료시켜준다.

  - Future사용시

    - Cancel(boolean)을 통해 특정 시간안에 작업이 끝나지 않는다면 cancel로 task를 종료시키거나 get()을 호출하여 CancellationException을 발생시켜, 예외 발생시 해당 스레드가 가지고 있는 리소스를 반환하는 식으로 구현(try with resource)

  - Spring Batch (Multithread-Step 사용시)

    - Step에서 taskExecutor 적용시
  
      - step에서의 taskExecutor설정은 TaskExecutor를 받게되는데 TaskExecutor에는 shutdown과 같은 메서드 없이 execute() 만 정의되어있어 다른 방법으로는 task가 종료되지 않는다.

      - ```java
        System.exit(SpringApplication.exit(SpringApplication.run(BatchApplication.class, args)));
        ```

        위처럼 main()메서드에 설정하게되면, 배치 작업이 끝날때까지 메인 스레드가 대기하였다가 jvm을 종료해주게 된다. 이는 실행되었던 작업이 성공적으로 실행되었다는 것을 보장한다.

    - @Async 적용시
  
      - @Async를 적용하게되면 spring batch와는 무관하게 비동기 작업이 수행되게 되고 spring container에서 ThreadPoolTaskExecutor를 관리하여 비동기 작업이 수행되기 때문에, 외부에서 해당 빈을 직접 주입받아 shutdown()작업을 수행해주어야한다.
  
      - ```java
        @Component
        @RequiredArgsConstructor
        public class ThreadPoolTaskExecutorShutdownJobExecutionListener implements JobExecutionListener {
            private final ThreadPoolTaskExecutor executor;
        
            @Override
            public void beforeJob(JobExecution jobExecution) {
            }
        
            @Override
            public void afterJob(JobExecution jobExecution) {
                executor.shutdown();
            }
        }
        
        // job 생성
        private final ThreadPoolTaskExecutorShutdownJobExecutionListener threadPoolTaskExecutorShutdownJobExecutionListener; 
                                                                                                                             
        @Bean                                                                                                                
        public Job sampleJob21() {                                                                                           
            return jobBuilderFactory.get("sampleJob21")                                                                       
                    .incrementer(new RunIdIncrementer())                                                                     
                    .start(asyncStep1())                                                                                      
                    .listener(threadPoolTaskExecutorShutdownJobExecutionListener)                                            
                    .build();                                                                                                
        }  
        ```
  
        배치 job에 대한 이벤트 인터페이스인 JobExecutorListener에서 beforeJob과 afterJob을 오버라이딩하여 실행중인 ThreadPoolTaskExecutor의 스레드를 제어해준다.
  
      - 혹은 위의 방법에서 처럼 ThreadPoolTaskExecutor의 설정(keepAliveSeconds, allowThreadTimeout)으로 task를 제어해준다.


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

- WAS가 실행되면 DB와 미리 Connection한 객체를 Pool에 저장하여 클라이언트 요청시 Pool에 저장된 Conection을 사용하고 반납하는 방식
- 사용이유
  - JDBC를 사용하기 위해서는 Driver로드-Connection생성-Statement로 질의생성-ResultSet 결과 매핑-종료의 과정을 거치게 된다. 이때 매번 Driver를 로드하고 Connection을 생성하는 것은 비용이 비싸기 때문에 미리 정의된 Connnection 개수만큼 생성하여 Pool에 저장하여 Connection 비용과 시간을 단축시킬 수 있다.
  - 과도한 Connection 생성으로 서버 자원 고갈을 막기 위함
  
- HikaripCP
  - 가벼운 용량과 빠른 속도를 가진 JDBC의 Connection Pool 프레임워크
  - 동작
    - Thread에서 Connection요청
    -  이전에 사용했던 Connection이 있는지 확인
    - 사용했던 Connection이 없다면 Connection Pool에 사용가능한 Connection이 있다면 커넥션 제공
    - Connection이 존재하지 않는다면, HandOffQueue Pooling을 하면서 다른 Thread의 Coinnection 반납을 대기한다.
      - 다른 Thread가 Connection을 반납하면 HandOfQueue에 Connection을 삽입하고 HandOfQueue Pooling하던 Thread에 Connection을 할당한다.
  
- Connection Pool 크기
  - MySQL : 600명에 15~20개의 Connection Pool
  - 모 테크 블로그 : Tn * (Cm - 1) +1
    - Tn : 총 스레드 개수
    - Cm : 하나의 Task에서 동시에 필요한 Connection 수


</details>

-----------------------

<br>



<br>

-----------------------

### @Retention

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- Retention어노테이션은 적용된 어노테이션의 라이프사이클을 결정해주는 어노테이션이다. 즉, 어노테이션이 어느 시점까지 살아있을 것인지 정해주는 역할
- RententionPolicy.SOURCE
  - 어노테이션이 소스 코드(.java)시점까지 살아있고 컴파일시 사라진다.
  - @Getter, @Setter 어노테이션에서 사용한다.
  - @Getter나 @Setter어노테이션은 소스코드상에서는 존재하지만 컴파일 시점에 사라지게 되는데, 그냥 사라지는 것이 아닌 컴파일 후 클래스 코드(.class = 바이트코드)에서는 getter, setter 코드가 바이트 코드로 생성되어있다.

- RetentionPolicy.CLASS
  - 어노테이션이 클래스 코드(.class)까지 살아있는 정책.
  - @NonNull과 같은 어노테이션등에 작용한다.
    - @NonNull은 파라미터에 적용되면 메소드 앞부분이나 생성자 바디 부분에 파라미터 null을 체크하는 로직이 삽입되고, 필드에 사용되면 필드에 값을 할당하는 메소드에 null 체크로직을 삽입한다.

  - **SOURCE나 RUNTIME에서 웬만하면 다 사용가능할텐데 CLASS정책이 있는 이유**
    - GRADLE에서 다운받은 라이브러리와 같이 .jar로 저장된 라이브러리에는 소스 코드(.java)가 없고 `클래스 코드(.class)로만 이루어져 있다`. 그렇기 때문에  클래스 코드 상에서 존재하는 어노테이션 정보를 사용하기 위해 필요한 정책.

- RetentionPolicy.RUNTIME
  - 어노테이션이 런타임 시점까지 살아있다.
  - @Component, @Entity 어노테이션등에서 사용한다.
  - 해당 정책은 Reflection API등과 같이 런타임 시점에 실행되는 작업에 대해서 어노테이션 정보를 사용하기 위한 정책인데, 런타임 시점에 스프링 컨테이너에 빈을 생성하고 등록하기 위해 @Component어노테이션을 찾아 탐색하고 Reflection API를 통해 빈을 생성하기 위한 방법으로 사용된다.



</details>

-----------------------

<br>



<br>

-----------------------

### RequestBody

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- RequestBody에는 Setter가 필요없다?

  - Post를 통해 RequestBody를 받을 때, `Jackson2HttpMessageConverter`에서 Json을 `ObjectMapper`를 이용해 매핑을 시켜주기 때문에 Setter는 필요없다.

    - Getter를 통해 매핑할 객체의 필드 정보를 얻는다.
    - ObjectMapper
      - ObjectMapper는 내부적으로 Reflection을 통해 기본생성자로 객체를 생성하고 Reflection이 필드를 set하여 초기화 한다.
        - Getter나 Setter 중 하나는 필수적이며, 주로 Getter를 사용한다.
        - 기본 생성자는 필수
      - `readValue([JSON String],[Object.class])`
      - `writeValue([생성할 파일],[object])`
        - object -> json : `writeValueAsString([object])`

  - Get에서는 RequestParam으로 object를 받을땐 Jackson2HttpMessageConverter가 아닌 `WebDataBind`에서 파라미터값을 받아준다. 이때, WebDataBind는 기본적으로 `initBeanPropertyAccess`메서드를 통해 파라미터와 객체를 매핑시켜주는데, 이는 `Java Bean`으로 등록해주기 때문에 Setter가 필요하게된다.
  
    - WebDataBind는 JavaBean을 따르기 때문에 Setter가 필요하다.
      - 기본 생성자 필수
      - 인스턴스 변수는 모두 private
      - Getter, Setter 필수
      - Serializable 선언
  
  - Get에서 Setter없이 파라미터를 객체로 매핑해주기 위해서는 `initDirectFieldAccess`로 빈 등록이 아닌 필드에 직접 접근해 할당하도록 한다.
  
    - 해당 방법을 사용한다면 Reflection을 통해 객체를 생성하기 때문에 Setter가 필요없어진다.
  
    - ```java
      @Slf4j
      @ControllerAdvice
      public class WebControllerAdvice {
      
          @InitBinder
          public void initBinder(WebDataBinder binder) {
              binder.initDirectFieldAccess();
          }
      }
      ```
  
- ModelAttribute

  - 요청을 받는 경우 RequestBody와 RequestParam뿐만 아니라 ModelAttribute도 있다.
  - ModelAttrubute는 폼 형태의 Http Body와 요청 파라미터를 생성자나 setter로 바인딩하기 위해 사용한다.
    - Reflection으로 인자가 있는 생성자를 찾고, 없다면 부분 인자의 생성자를 찾고 그렇지 않다면 기본 생성자로 객체를 생성하고 setter로 필드를 추가해준다.
  - ModelAttribute는 폼형태의 body와 요청 파라미터를 객체로 받아주는 역할을 한다.
    - ModelAttribute는 파라미터 접근 방법을 사용한다.(initBeanPropertyAccess)
      - 기본 생성자로 인스턴스 생성
      - setter를 통해 필드 주입
      - 만약 해당 모든 필드를 주입하는 생성자를 사용한다면 setter를 사용하지 않고 객체를 생성할 수 있다



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

- 데이터에 영속성을 부여하는 프레임워크
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
  - 객체와 SQL 필드를 매핑시켜주는 기술
  - 객체와 테이블을 매핑해주는 것이 아닌 SQL결과를 어떤 객체에 바인딩하는 기술
  - 장점
    - SQL을 그대로 사용하기 때문에 복잡한 SQL에 강하다.
  - 단점
    - DBMS에 종속적이다.
    - 간단한 쿼리도 직접 작성해줘야한다.
  
- ORM (Object Relation Mapping)
  - 객체와 객체형 데이터베이스를 매핑시켜주는 기술
  - 장점
    - 객체지향적인 코드로 인해 더 직관적이고 비즈니스 로직에 더 집중할 수 있게 도와준다.
    - 재사용 및 유지보수의 편리성이 증가한다
    - 데이터베이스에 종속적이지 않는다.
    
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
  
- 쿼리 작성

  - statement

    - ```java
      try {
          Connection conn = null;
          Statement stmt = null;
           
          String sql = "INSERT CUSTOMER (NAME, AGE, ADDRESS) VALUES('" + name +"'," + age + ",'" + address +"')";
           
          conn = DriverManager.getConnection("jdbc:oracle:thin:@" + ip + ":" + port + ":" + sid, id, password);
          stmt = conn.createStatement();
          stmt.executeQuery(sql);
           
          stmt.close();
          conn.close();
      } catch(Exception e) {
          e.printStackTrace();
      }
      ```

    - statement로 쿼리를 작성할때 String타입으로 쿼리를 작성하고 매개변수를 중간에 문자열 연산을 통해 작성을 해주게된다.

    - Sql inject와 같이 보안에 취약하고 가독성이 좋지 못하다.

  - prepareStatement

    - ```java
      try {
          Connection conn = null;
          PreparedStatement pstmt = null;
           
          String sql = "INSERT CUSTOMER (NAME, AGE, ADDRESS) VALUES(?, ?, ?)";
           
          conn = DriverManager.getConnection("jdbc:oracle:thin:@" + ip + ":" + port + ":" + sid, id, password);
          pstmt = conn.prepareStatement(sql);
           
          pstmt.setString(1, name);
          pstmt.setInt(2, age);
          pstmt.setString(3, address);
           
          pstmt.executeUpdate(sql);
           
          stmt.close();
          conn.close();
      } catch(Exception e) {
          e.printStackTrace();
      }
      ```

    - prestatement는 statement와 다르게, 매개변수를 문자열 연산으로 작성해주지 않고 set을 이용해 빌더 형식으로 매개변수를 적용해준다.

    - 코드의 안전성과 가독성을 높여줄수 있다.


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
  - Spring JDBC의 접근 방법 중 하나, JDBC API를 사용하여 데이터에 접근할 수 있게 하며 JDBC의 과정을 대신 처리해주고 `DataSource 설정, 쿼리 작성, 결과 처리` 만 해주면 된다.
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
      - 객체 저장시 자동으로 부모 테이블과 자식 테이블을 저장하는 쿼리를 만들어 주어 저장된다.
    - 연관관계
      - 참조객체와 함께 객체를 저장하면 자동으로 참조를 외래키로 변경하여 쿼리를 만들어 준다.
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

- JPA의 구현체 중 하나로 Hibernate 내부의 JDBC API를 통해 데이터베이스와 통신하는 Persistence 프레임워크.
- JPA를 이용해 POJO원칙의 비즈니스 오브젝트에서 Object와 RDB매핑을 사용할 수 있게 해준다.
- 특정 클래스에 매핑되는 테이블에 대한 관계가 정의되어있는 XML메타데이터를 통해 관계객체 매핑을 간단하게 수행한다.
- HQL (Hibernate Query Language)
  - HQL은 SQL과 유사하지만 SQL에서 지원하지 않는 페이지네이션과 같은 고급 기능을 제공한다.
  - HQL은 객체지향으로써 상속, 다형성 등의 객체지향 강점을 누릴 수 있다.
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
- `select m from Member`
- ~~엔티티가 영속성 컨텍스트에만 저장된 상태로 조회하면 DB에 조회 데이터가 존재하지 않기 때문에 조회되지 않는다.~~
  - ~~JPQL로 조회시 DB에 SELECT쿼리가 요청되는 것이므로 DB에는 해당 데이터가 존재하지 않고 영속성 컨텍스트에만 존재하기 때문에 조회되지 않는다.~~



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
- 객체와 SQL의 필드를 매핑시켜주는 기술
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
  - 비용이 비싸기 때문에 일반적으로 하나의 EntityManagerFactory를 생성해서 사용한다.  (싱글톤 방식)
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
      - id생성전략이 Identity인 경우 Insert는 쓰기지연이 적용되지 않는다.
    - flush
      - 영속성 컨텍스트의 엔티티와 데이터베이스의 테이블을 동기화 하는 작업
      - 직접 사용, JPQL사용, 트랜잭션 commit시 자동 실행된다.
      - flush후 commit을 해주어야 데이터베이스에 트랜잭션 작업이 저장된다.
    
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

  | 종류         | 진행중인 트랜잭션 유                     | 진행중인 트랜잭션 무 | 특징                                                         |
  | ------------ | ---------------------------------------- | -------------------- | ------------------------------------------------------------ |
  | REQURED      | 해당 트랜잭션 사용                       | 새로운 트랜잭션 생성 | Default, 예외 발생시 롤백되고, 호출한곳도 롤백               |
  | MANDATORY    | 해당 트랜잭션 사용                       | 예외 발생            |                                                              |
  | REQUIRED_NEW | 해당 트랜잭션 보류, 새로운 트랜잭션 생성 | 새로운 트랜잭션 생성 | 별도의 트랜잭션 독립<br />자식 트랜잭션에서 예외 발생시, 부모에서 처리해준다면 자식 트랜잭션 호출전 작업까지만 커밋 |
  | SUPPORTS     | 해당 트랜잭션 사용                       | 트랜잭션 없이 실행   | 엔티티 조회시 propagation은 supports와 read-only를 사용하는것이 성능적으로 좋다. |
  | NOT_SUPPORT  | 해당 트랜잭션 보류                       | 트랜잭션 없이 진행   | Read-only를 사용할때 사용하면 성능적으로 좋다.               |
  | NEVER        | 예외 발생                                | 트랜잭션 없이 진행   |                                                              |
  | NESTED       | 중첩 트랜잭션 생성                       | 새로운 트랜잭션 생성 | 부모 트랜잭션이 롤백되면, 중첩 트랜잭션도 함께 영향을 받아 롤백된다.<br /> 중첩 트랜잭션이 롤백되면 부모 트랜잭션은 영향을 받지않고 커밋된다. |

  

</details>

-----------------------

<br>



<br>

-----------------------

### Propagation 주의사항

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- Propagation.REQUIRED
  - REQUIRED는 기존 트랜잭션이 존재한다면, 해당 트랜잭션을 그대로 사용한다. 연속으로 사용하는 트랜잭션을 내부 트랜잭션이라고 명시한다면, 
  - 내부 트랜잭션에서 예외를 발생시킨다면 해당 트랜잭션에서 rollback-only 마킹을 하게된다. 내부 트랜잭션에서 예외 작업처리를 완료했고 메인 트랜잭션에서 작업을 마무리하려고 commit을 수행하게되면 이미 내부 트랜잭션에 의해 해당 트랜잭션이 rollback 마킹이 되어버렸기 때문에 재활용(작업 완료)가 되지 않게된다.
  - 이를 해결하기 위해서는 NESTED정책을 사용해주어야한다.

- Propagation.NESTED
  - 기존 트랜잭션이 있다면, 중첩 트랜잭션을 수행해주게 된다.
    - 기존 트랜잭션에 save point를 지정해주고 내부적으로 새로운 트랜잭션을 수행해준다.

  - 해당 정책은 부모 트랜잭션에 예외가 발생한다면 둘다 롤백되지만, 중첩 트랜잭션에 예외가 발생한다면, 중첩 트랜잭션만 롤백이 수행되고 부모 트랜잭션은 롤백이 수행되지 않는다.
  - 그렇기 때문에 중첩 트랜잭션의 예외로 부모 트랜잭션이 영향을 받지 않기 때문에 REQUIRED에서 발생한 문제를 해결할 수 있다.
  - 하지만 Hibernate에서는 NESTED를 지원해주지 않는다. DataSourceTransactionManager를 직접 사용할때만 지원해준다.
    - (예상) JPA에서는 변경감지를 통해 업데이트를 지연해서 수행하기 때문에 트랜잭션 경계를 설정할 수 없기 때문에 savepoint를 지원해주지 않는듯하다.
    - JDBC 3.0 이상부터 NESTED를 지원해준다고한다.
  
- https://techblog.woowahan.com/2606/
- https://reiphiel.tistory.com/entry/understanding-of-spring-transaction-management-practice


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
  - ~~쿼리 메소드 사용시 조회 주체에 대한 select 쿼리가 생성되기 때문에 연관 엔티티 조회를 하기 위한 select 쿼리가 추가 생성되기 때문이다.~~

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
    - <img width="392" alt="image" src="https://user-images.githubusercontent.com/57162257/196611283-5fe908c2-4398-4648-a50a-72f89cce905a.png">
  
- EntityGraph `(outer join)`
  - 쿼리 메소드에 @EntityGraph 어노테이션을 사용하여 attributePaths 속성에 연관 엔티티 필드 값을 작성하고 join 없이 JPQL을 작성한다.
  - <img width="514" alt="image" src="https://user-images.githubusercontent.com/57162257/196611154-c915d225-16a3-485c-871d-4c9eabc6b6a7.png">
  - JPQL에 inner join을 작성하면 inner로 참조 엔티티를 불러올 수 있다.


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

- 비즈니스 로직상에서의 작업을 하나의 작업단위로 트랜잭션 처리를 수행할수 있도록 제공하는 기술
- @Transactional을 적용하면 타겟 객체를 상속한 프록시 객체가 생성되고 프록시 객체가 빈으로 등록된다.
- 코드레벨의 트랜잭션을 처리하기 위한 connection, commit, rollback과 같은 코드 작성을 줄여 중복코드를 방지하고, 서비스 레이어에 핵심적 관점 코드만 존재하여 가독성을 높일 수 있다.
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

### @Transactional 읽기 전용

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- JPA를 이용해 엔티티가 영속성 컨텍스트에 의해 관리되면 1차캐시, 지연 로딩 등 많은 이점을 제공해주게 된다. 하지만 더티 체킹을 위해 1차 캐시에 있는 엔티티의 스냅샷을 찍어 메모리에 저장해 놓기 때문에 메모리 성능으로는 좋지 못할 수 있다.
- 읽기 전용을 사용하게 된다면 스냅샷을 저장하지 않고 엔티티의 영속성 여부만 판단하면 되기 때문에 메모리 성능을 향상시킬 수 있는 장점이 있다.
- 읽기 전용 방법
  - 엔티티가 아닌 스칼라 타입으로 특정 필드만 선택해서 조회
    - `SELECT o.id, o.name FROM Order o`
    - 스칼라 타입 : 하나의 데이터만 읽을수 있는 타입
  - 읽기 전용 트랜잭션 사용
    - @Transactional(readOnly = true)
- readOnly = true 이유
  - 데이터가 의도치않게 변경되는 것을 방지해준다.
  - 스냅샷, 더티체킹을 수행하지 않아 성능 향상
  - 디비 서버가 이중화 되어있을때 읽기 노드인 slave에 요청되어 트래픽을 분산시켜줄수 있다
  - 직관적으로 읽기 전용이라는 의미를 전달할수 있다.



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
  - QueryDsl은 엔티티를 기준으로 쿼리를 작성하기 때문에 type safe하게 쿼리를 작성하여 컴파일시 에러를 발생시킨다.
- 동작원리
  1. 컴파일 단계에서 @Entity어노테이션을 선언한 클래스를 탐색하고 JPAAnnotationProcessor를 통해 쿼리 타입(Q Class)생성
  2. 쿼리 타입(Q Class)으로 도메인 클래스의 메타데이터를 전달하여 엔티티를 타겟으로 쿼리를 작성하게 된다.

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
- 해결방법
  - 양방향 onetoone이 필요한지 고려하기
  - 꼭 써야한다면 onetoone이 아닌 onetomany관계로 구조 바꿔보기
  - 구조를 유지해야한다면 fetch join, batch size 사용하기


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

### @GeneratedValue

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- IDENTITY
  - 기본키 생성을 DB에 위임하는 전략
  - Auto Increment를 지원해주는 데이터베이스에 사용(MySQL, MariaDB, PostgreSQL)
  - id를 null로 저장할때, 영속성 컨텍스트 1차 캐시에 엔티티를 저장해주기 위해서는 id값이 필수인데 IDENTITY전략은 기본키 생성을 DB에 위임했기 때문에 INSERT 쿼리를 생성해서 기본키를 받아온 후 1차 캐시에 엔티티를 저장한다.
    - 즉, IDENTITY전략에서 INSERT는 쓰기지연을 지원해주지 않는다.

- SEQUENCE
  - 유일한 값을 순서대로 생성하는 특별한 데이터베이스 오브젝트
  - Sequence를 지원해주는 데이터베이스에 사용 (Oracle, MariaDB, PostgreSQL)
  - id를 null로 저장할때, 마찬가지로 영속성 컨텍스트 1차 캐시에 엔티티를 저장해주기 위해서는 id값이 필수인데, SEQUNCE전략은 데이터베이스에 생성한 시퀀스 오브젝트에 call next를 통해 다음 seq(식별자)를 가져오고 엔티티에 적용한 후 1차 캐시에 엔티티를 저장한다.
  - seq를 불러오기 위해 매번 데이터베이스와 연결하는것은 비효율적이기 때문에 allocationSize를 통해 불러오고 싶은 seq의 개수를 선언하고 한번 불러올때 설정한 seq개수 만큼 메모리에 저장하고 엔티티를 영속성 컨텍스트에 저장할때 사용한다.
    이후 캐싱된 seq를 모두 사용하였다면 seq 개수만큼 다시 요청하여 메모리에 저장하여 효율적으로 사용할 수 있게 된다.
    - 단점 : seq를 한번에 불러와 캐싱하였기 때문에 서버가 종료된다면 데이터베이스의 시퀀스 오브젝트는 유지되어 사용되지 않는 seq는 버려지게 된다.

- TABLE
  - 기본 키 전용 테이블을 생성하여 사용하는 방법
  - 모든 데이터베이스에 사용가능하지만 최적화된 방법이 아니기 때문에 성능상 이슈가 있을 수 있다.

- AUTO
  - hibernate에서 키 생성전략을 자동으로 설정해준다.


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

- 도메인
  - 소프트웨어로 해결하고자하는 문제
- 도메인 모델
  - 도메인을 개념적으로 표현한 것.
  - 도메인 모델을 통해 개발자, 기획자가 동일한 모습으로 도메인을 이해하고, 도메인의 지식을 공유하는데 도움이 된다.
- 도메인 모델 패턴
  - 객체지향 기반으로 도메인을 구현하는 패턴
  - 비즈니스 로직을 도메인에 직접 작성하는 방식(도메인에 데이터와 비즈니스 로직이 함께 존재한다)
  - 객체간 관계를 맺을 수 있어, 제약이 가능하고 로직이 단순해진다.
  - 객체들간의 설계가 수반되어야 하기 때문에 모델 구축이 어렵다.
- 도메인 주도 설계
  - 도메인별로 나누어 설계하는 방식
  - 모두의 프로젝트 이해와 커뮤니케이션 수단의 통일성(도메인)을 만들어 기획자부터 개발자까지 프로젝트 커뮤니케이션 비용 낭비를 최소화 하기 위한 설계 방법론
- DDD 아키텍처
  - WebLayer
    - 컨트롤러와 뷰의 영역으로 외부와의 연결이 가능한 영역.

  - ServiceLayer
    - 컨트롤러와 DAO 중간 영역이 위치
    - 트랜잭션, 도메인간 순서를 보장하주는 역할

  - RepositoryLayer
    - DB와 같은 저장소에 접근하는 영역 (DAO)

  - Domain Model
    - 개발 대상이 되는 도메인을 개념적으로 표현한것으로서, 기획자와 개발자가 동일한 모습의 도메인으로 이해하고 도메인 정보를 공유하기 쉽게 하기 위해 단순화 한것.
    - 실제 비즈니스 로직이 실행되는 곳

- 트랜잭션 스크립트 패턴
  - 트랜잭션 스크립트
    - 하나의 트랜잭션으로 구성된 로직을 서비스 계층에서 모두 작성하는 방법
    - 장점
      - 구현이 쉽다

    - 단점
      - 비즈니스 로직이 복잡해지면 난잡한 코드가 된다.
      - 중복 코드가 발생한다

  - 도메인 모델 패턴
    - 객체지향 설계에 기반하여 구현하고자하는 도메인의 모델을 생성하는 패턴
    - 도메인 내부에 데이터와 비즈니스 로직이 함께 존재한다.
    - 장점
      - 객체 지향에 기반한 재사용성,확장성, 유지보수가 좋다

    - 단점
      - 객체들간의 설계가 수반되기 때문에 모듈 설계가 어렵다



</details>

-----------------------

<br>





<br>

-----------------------

### Gradle vs Maven

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

- Maven
  - 자바용 프로젝트 관리 도구
  - POM으로 사용되며 pom.xml을 통해 프로젝트 정보, dependency와 의존 dependency를 설정한다.

- Gradle
  - 프로젝트 구성/관리, 빌드, 배포 도구
  - AntBuilder와 Groovy를 통해 유연한 정의가 가능하다.
    - Groovy : JVM에 독자적으로 실행되는 스크립트 언어로써 컴파일 필요없이 실행이 가능하다.

- 차이
  - maven은 xml로 의존성을 정의하고 사용하지만 Gradle은 groovy를 통해 플러그인을 호출하여 쉽게 빌드할수 있으며 if, while등의 변수를 사용하여 유연하고 간결하게 정의가 가능하다.
  - 가독성이 maven보다 gradle이 훨씬 좋다


</details>

-----------------------

<br>



<br>

-----------------------

### DTO에서 필드값을 원자값이 아닌 클래스타입을 사용하는가?

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- 원자값을 사용하게 되면 기본값이 0으로 설정된다. 그렇기 때문에 값이 없다면 null이 아닌 0으로 표시되기 때문에 0의 값을 가지는지 null인데 0으로 변한건지 구분할수가 없기때문에 null을 구분하기 위한 클래스타입으로 선언해주는것.



</details>

-----------------------

<br>



<br>

-----------------------

### @NotNull, @NotEmpty, @NotBlank

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

### 클린코드

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- 가독성을 추구하여 직관적으로 이해할 가능성이 높은 코드를 말한다.
- 코드는 읽는것이 아닌 해석하는 것이기 때문에, 코드를 처음 보는 사람이 코드를 해석하는 비용이 최소화 될수록 클린 코드이다.
  - 코드를 처음보는 사람 : 유지보수자, 3개월뒤 작성된 코드를 보는 나

- 가독성을 추구하기 위해 표현적 가독성과 기능적 가독성을 구분한다.
  - 표현적 가독성
    - 눈에 잘 들어오는 코드로, 코드 컨벤션을 정하거나 함수를 통해 짧게 구성한다.(SRP - 단일 책임)

  - 기능적 가독성
    - 변수, 함수, 클래스 등이 어떤 역할을하고 어떤 동작을 하고 서로 어떤 관계를 가지는지 직관적으로 파악할 수 있는 코드
    - 의미있는 네이밍이나 함수의 추상화를 통해 가독성을 높일 수 있다.
      - 코드를 한곳에 길게 쓰는것이 아니라 각 역할을 나누어 함수로 구분하여 작성하는것.

- 장점
  - 유지보수 시간이 줄어든다.
    - 가독성 좋은 코드는 코드 리뷰나 디버깅 시간을 단축 시킬 수 있다.
    - 시간 == 돈




</details>

-----------------------

<br>



<br>

-----------------------

### CI/ CD

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- CI/CD는 애플리케이션 개발 단계를 자동화 하여 애플리케이션을 사용자에게 짧은 주기로 전달하는것
- CI (Continuous Integration)
  - 지속적인 통합으로써, 개발자가 코드를 수정하고 병합하면 자동적으로 코드가 정상작동하는지 빌드하고 테스트를 수행하는것.

- CD (Continuous Deploy)
  - 지속적인 배포로써, CI를 통해 검증이 끝난 코드를 자동으로 실제 배포를 수행해주는 것




</details>

-----------------------

<br>
