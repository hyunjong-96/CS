# Spring Security



<br>

-----------------------

### Spring Security

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

- 자바 애플리케이션에서 인증, 인가를 처리하고 보호 기능을 제공하는 프레임워크

- spring security 사용시 애플리케이션에 인증, 인가, 보호 기능을 자체적으로 구현할 필요없이 다양한 기능을 확장할 수 있습니다.

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
  - Security Filter는 서블릿 컨테이너의 Filter와 마찬가지로 DispatcherServlet 요청 전에 사용되는 필터이다.
  - Security Filter는 서블릿 컨테이너의 Filter Chain에 DelegatingFilterProxy를 등록하고 delegatingFilterProxy는 빈으로 등록된 SecurityFilterChain에게 필터 작업을 위임한다. (스프링 컨테이너의 filter 작업 전체 작업 위임 x, security filter 작업 위임 o)
  - 방법
    - WebSeucrityConfiguerAdapter라는 Filter chain을 구성하는 클래스를 상속받아 Configure클래스를 생성하고configure() 를 오버라이딩하여 filter chain을 구성할 수 있다.
    - 현재 WebSecurityConfigureAdapter클래스가 deprecate당해서 새로운 방법을 사용해야한다 (공부해야함)
      - 바뀐 버전에서는 WebSecurityConfigureAdapter대신, SecurityFilterChain을 빈으로 등록하여 사용해야한다.
      - https://velog.io/@pjh612/Deprecated%EB%90%9C-WebSecurityConfigurerAdapter-%EC%96%B4%EB%96%BB%EA%B2%8C-%EB%8C%80%EC%B2%98%ED%95%98%EC%A7%80
  - 종류
    - SecurityContextPersistenceFilter : HttpSecurityContextRepository를 통해 Session에 SecurityContext가있는지 확인하고 존재한다면 해당 SecurityContext를 SecuirtyContextHolder에 저장하고 thread-local에 저장한다.
      - 인증 전
        1. HttpSecurityContextRepository에서 SecurityContext를 생성한다.(현재는 null)
        2. 인증 필터에서 인증완료후 Authentication을 생성하고 SecurityContext에 저장한다.
        3. 응답 전에 Session에 SecurityContext를 저장하고 SecurityContext를 초기화한다.
      - 인증 후
        1. Session에서 SecurityContext를 가져온다.
        2. SecurityContextHolder에 SecurityContext를 저장한다.
    - UsernamePasswordAuthenticationFilter : login요청을 감시하며 인증과정 진행.
    - SessionManagementFilter : 사용자의 동시로그인 제한 등의 기능을 제공
    - ExceptionTranslationFilter : 내부적으로 FilterSecurityInterceptor를 사용하여 AuthenticationException또는 AccessDeniedException을 받는다면 예외를 처리해준다.
      - AuthenticationEntryPoint : 인증되지 않은 사용자가 요청했을 경우 AuthenticationException을 받고 AuthenticationEntyPoint를 실행하여 401과 함께 인증을 유도한다.
      - AccessDeniedHandler : 권한이없는 기능을 사용할 경우 AccessDeniedException을 받고 AccessDeniedHandler을 실행하여 403을 보낸다.
    - FilterSecurityInterceptor : 인가처리 담당 필터
      - 요청정보(URI), 권한정보(hasRole), 인증정보(SecurityContextHolder)를 통해 요청한 리소스에 대한 권한 여부를 확인한다.
      - 인증되지 않은 사용자가 보호된 자원에 접근시 AuthenticationException발생
      - 인증된 사용자가 권한이없는 자원에 접근시 AccessDeniedException발생
      - 위 두 예외가 발생하면 ExceptionTranslactionExceptionFilter를 통해 각각 401과 403예외를 반환


</details>

-----------------------

<br>



<br>

-----------------------

### AuthenticaionManger & AuthenticationProvider

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

- AuthenticationManager
  - 인증 필터로 부터 인증 요청을 받게되면 인증처리자(AuthenticationProvider)중 해당 인증이 처리가능한 provider를 찾아 인증을 위임하게된다. 인증이 완료되면 Authentication을 전달한다.

- AuthenticationProvider
  - 인증 처리를 담당하는 인터페이스로서, 인증을 처리하는 authentication메서드와 인증처리 가능한 provider인지 검사하는 support메서드를 정의한다.
    - authentication메서드 로직
      - UserDetailsService에서 UserDetails를 가져와 아이디 인증, 패스워드 인증 등을 수행하고 인증된 Authentication을 전달한다.



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

- Filter는 서블릿 컨테이너에서 관리되며 Bean은 스프링 컨테이너에서 관리됩니다. 그렇기 때문에 Filter는 bean을 사용할 수 없습니다.
- DelegatingFilterProxy 클래스를 사용하면 DelegatingFilterProxy는 Bean으로 등록된 SecurityFilterChain이 서블릿 필터에서 수행될 수 있도록 역할을 위임해줍니다.
- <img width="793" alt="image" src="https://user-images.githubusercontent.com/57162257/188792052-861b0054-5160-4bcf-8cdf-8429dadcfab5.png">

</details>

-----------------------

<br>



<br>

-----------------------

### 인증 저장소

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />







-----------------------

- SecuirtyContext
  - Security에서 인증된 객체는 일반적으로 Security Context에 저장되고 Secuirty Context는 Security Context Holder에 저장됩니다.
  - 인증된 객체가 저장된  SecurityContextHolder는 thread local에 저장되기 때문에 각 스레드에서 전역적으로 사용자 정보를 사용할 수 있고 각 스레드 별로 다른 인증객체를 가질 수 있습니다.
    - thread local : 스레드에서 독립적으로 사용할 수 있는 지역변수
    - <img width="685" alt="image" src="https://user-images.githubusercontent.com/57162257/188788345-780eff5e-0af6-43e2-aa9b-e1bf34229dcf.png">
- SecuirtyContextHolder
  - 인증된 객체인 Authenticaion을 저장하는 SecurityContext를 감싸고 있는 Wrapper Class입니다.
  - SecurityContext 저장 방식을 설정해 줄 수 있습니다
    - Thread_Local : 스레드당 security context 할당
    - Inheritable_Thread_Local : 부모 스레드와 자식스레드가 동일한 security context를 가집니다.
    - Global : 메모리에서 하나의 SecurityContext 참조
- <img width="1034" alt="image" src="https://user-images.githubusercontent.com/57162257/188788414-2ff61688-e20e-4bfb-ae40-148c4e9bf024.png">
- `Authentication authentication = SecurityContextHolder.getContext().getAuthentication()`

</details>

-----------------------

<br>



<br>

-----------------------

### Security에서 Session 유지 방법

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />
  


-----------------------

- 요청이 들어오게 되면 SecurityContextPersistenceFilter에서 HttpSessionSecurityContextRepository를 통해 인증 여부를 확인합니다.
- 인증 전에는 UsernamePasswordAuthenticationFilter에서 사용자를 인증하고 인증된 객체인 Authentication을 SecurityContext에 저장합니다. 그리고 사용자에게 응답하기 전에 Session에 SecurityContext를 저장하고 인증된 정보를 사용합니다.
- 인증 후에는 Session의 SecurityContext를 불러와 thread local에 SecurityContext를 담은 SecurityContextHolder를 저장하고 인증된 정보를 사용합니다.
- https://devlog-wjdrbs96.tistory.com/404

</details>

-----------------------

<br>



<br>

-----------------------

### CORS & CSRF & XSS

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- CORS (Cross Origin resource sharing)
  - 교차 출처 리소스 공유
  - 다른 출처(domain)로 URL을 요청하여 리소스를 가져오는 것.
  - 서버에서는 응답시 access-control-allow-origin에 허용된 도메인을 보내고 사용자의 웹 브라우저는 요청때 보낸 origin에서 출처의 도메인과 비교한다.

- CSRF (Cross Site Request Forgery)
  - 사이트간 위조 요청
  - 사용자가 메일이나 링크를 누르게 되면 Put, Delete로 서버에 악의 요청을 보내는 것.
  - 서버에서는 요청 헤더의 referer에 등록되어 있는 요청 domain정보를 확인하여 올바른 domain에서 요청이 들어왔는지 확인하거나,
    Csrf-token을 사용해서 사용자가 요청시 csrf-token이 올바른지 판단하여 검증하는 방법
    - 서버에서 생성된 곳에서 요청을 보내고있음을 증명한다.(referer, csrf-token)
  
- XSS (Cross Site Scripting)
  - 공격자가 상대방이 자주사용하는 웹사이트에 악성 스크립트를 삽입하여 사용자가 악성 스크립트가 포함된 게시글을 사용했을 때 공격자에게 사용자의 쿠키 정보를 탈취하여 사용자 정보를 도용하거나 해당 사이트에 악의적 요청을 보내는것.
  - 사용하고 있는 웹 사이트 이상한 점은 없는지 이상한 URL로 접속해있는지 확인해야한다.

</details>

-----------------------

<br>





---

## 면접 예상 질문

---



<br>

-----------------------

### Spring Security 란 무엇인가요

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- Spring Security란 자바 애플리케이션에서 인증, 인가 처리 및 cors, csrf 등으로 부터 보호 기능을 제공하는 프레임워크입니다.
- spring security를 사용하면 애플리케이션 보호에 대한 기능을 자체적으로 구현할 필요없고 기능을 확장시킬 수 있습니다.

</details>

-----------------------

<br>



<br>

-----------------------

### Spring Security는 왜 사용하셨나요?

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- 인증, 인가를 처리 기능을 사용하기 위해 spring security를 사용했으며 Interceptor나 AOP가 아닌 Filter로 공통 인증 기능을 구현해보기 위해 사용했습니다.

</details>

-----------------------

<br>



<br>

-----------------------

### 일반적 Spring Security 인증 프로세스

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

1. 요청이 들어오게 되면 Servlet이 호출되기 전에 Security Filter에서 요청을 가로챕니다.
2. AuthenticationFilter 에서 요청을 가로채고 인증용 객체인 UsernamePasswordAuthenticationToken을 생성합니다.
3. UsernamePasswordAuthenticationToken은 AuthenticationManger의 구현체인  ProviderManger에게 보내집니다.
4. ProviderManger는 다시 AuthenticationProvider에게 UsernamePasswordAuthentcationToken을 전달합니다.
5. AuthenticationProvider는 데이터베이스에 접근하여  사용자 인증 정보를 가져오는 UserDetailsService에 사용자 정보를 전달합니다.
6. UserDetailsService는 데이터베이스에서 사용자 정보를 가져와 사용자 인증 정보인 UserDetails를 반환합니다.
7. AuthenticationProvider는 사용자 정보를 비교하고 인증객체인 Authentication을 생성해 반환합니다.
8. Authentication은 AuthenticationFilter까지 반환되고 인증 객체를 SecurityContext에 저장하여 세션을 유지시킵니다.

</details>

-----------------------

<br>



<br>

-----------------------

### Security Context에 대해서 설명해달라.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />







-----------------------

- Jwt를 이용한 인증, 인가 처리를 위해 토큰 생성, 유효성 검사, 인증을 위한 JwtTokenProvider를 구현하고, 사용자 인증 정보를 가져오기 위해 User도메인에 UserDetails를 상속하여 구현했습니다. 그리고 JwtTokenProvider를 사용하기 위해 UsernamePasswordAuthenticaionFilter이전에 custom한 JwtAuthenticationFilter를 생성했습니다.

</details>

-----------------------

<br>



<br>

-----------------------

### Spring Security는 어떻게 사용했는지

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- Jwt를 이용한 인증, 인가 처리를 위해 토큰 생성, 유효성 검사, 인증을 위한 JwtTokenProvider를 구현하고, 사용자 인증 정보를 가져오기 위해 User도메인에 UserDetails를 상속하여 구현했습니다. 그리고 JwtTokenProvider를 사용하기 위해 UsernamePasswordAuthenticaionFilter이전에 custom한 JwtAuthenticationFilter를 생성했습니다.

</details>

-----------------------

<br>



<br>

-----------------------

### JWT를 Sprin Security에 적용한 이유

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- 일반적인 Spring Security는 Security Context에 저장된 Authentication으로 세션을 별도의 스레드를 돌려 유지하기 때문에 유지비용이 들고 서버에서 관리하기 때문에 인증 과정이 상대적으로 무겁습니다.
  하지만 JWT를 사용하게 되면 사용자의 정보는 서버 비밀키로 암호화되어 있고 토큰의 유효성 검사 후 해당 정보를 사용하기만 하면 됩니다. 그렇기 때문에 세션이 필요없게 되어 유지비용이 없고 가벼운 인증이 가능해집니다.
- 방법
  - WebSecurityConfiguration에서 season management의 sessionCreationPoliy속성을 stateless로 선언하여 세션을 사용하지 않는다고 선언한다.


</details>

-----------------------

<br>



<br>

-----------------------

### Filter와 Security Filter 차이점

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- 일반적으로 Filter는 spring context외부에 있으며 서블릿 컨테이너 filter에 직접 등록하여 사용합니다.
  Security Filter는 DelegatingFilterProxy를 서블릿 컨테이너 필터에 등록하여 일반 filter작업을 Security Filter Chain으로 위임받아 UsernamePasswordAuthenticationFilter, SessionManagementFilter, ExceptionTranslationFilter 등이 차례로 실행됩니다.

</details>

-----------------------

<br>



<br>

-----------------------

### Filter와 Intercepter 차이

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- Filter는 spring context외부에 존재하며 서블릿이 호출되기 전에 요청을 가로채 공통 보안 기능이나 이미지 압축,변환 등을 수행합니다.
- Intercepter는 spring context내부에 존재하며 서블릿이 컨트롤러를 호출하기 전에 요청을 가로채 공통 작업을 수행합니다.

</details>

-----------------------

<br>



<br>

-----------------------

### principle에는 어떤 정보가 들어가 있나요

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- 인증 프로세스 후 생성되는 인증 객체인 Authentication은 principal, credentials, authority로 구성되어있으며 principal은 사용자의 식별 데이터, credentials은 암호, authority는 권한을 가지고 있습니다.
- Authentication으로 등록된 principal은 컨트롤러 컴포넌트에서 파라미터로 가져올수 있다. (@AuthenticationPrincipal)

</details>

-----------------------

<br>



<br>

-----------------------

### spring security에서 사용해본 어노테이션

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- @EnableWebSecurity 어노테이션을 security config 클래스에 설정하여  security에 필요한 설정을 선언하였습니다.
- 인증된 사용자의 정보를 사용하기 위해 @AuthenticationPrincipal을 사용해 컨트롤러의 메소드에서 파라미터로 사용자의 정보를 받아왔습니다.

</details>

-----------------------

<br>



<br>

-----------------------

### Spring Security를 사용하면서 어려웠던 점과 아쉬웠던점

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />






-----------------------

- 어려웠던점
  - 가장 어려웠던 점 중 하나는 spring security에서 jwt를 적용하는데 인증 프로세스 구조와 개념이 완전히 자리 잡지 못한 상태에서 기능의 데드라인을 맞추고자 서툴렀던 탓에 원하는 인증, 인가처리 프로세스를 제대로 적용시키지 못하여 많은 시간을 보냈었던것이 가장 힘들었던것 같습니다..

- 아쉬웠던점
  - 앱 서비스에 대한 서버였기때문에 spring security에서 지원하는 cors, csrf 등과 같은 보호 기능 등 해당 서비스에 사용되지 않기 때문에 security에서 제공하는 기능을 더많이 경험해보지 못한것이 아쉬웠습니다.


</details>

-----------------------

<br>



https://imbf.github.io/interview/2021/03/06/NAVER-Practical-Interview-Preparation-8.html

https://velog.io/@gmtmoney2357/%EC%8A%A4%ED%94%84%EB%A7%81-%EC%8B%9C%ED%81%90%EB%A6%AC%ED%8B%B0-Authentication-SecurityContext

https://ugo04.tistory.com/167



https://catsbi.oopy.io/f9b0d83c-4775-47da-9c81-2261851fe0d0