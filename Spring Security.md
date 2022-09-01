# Spring Security



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
  - Security Filter는 서블릿 컨테이너의 Filter와 마찬가지로 DispatcherServlet 요청 전에 사용되는 필터이다.
  - Security Filter는 서블릿 컨테이너의 Filter Chain에 DelegatingFilterProxy를 등록하고 delegatingFilterProxy 내부 필터 체인에게 필터 작업을 위임한다. (스프링 컨테이너의 filter 작업 전체 작업 위임 x, security filter 작업 위임 o)
  - 방법
    - WebSeucrityConfiguerAdapter라는 Filter chain을 구성하는 클래스를 상속받아 Configure클래스를 생성하고configure() 를 오버라이딩하여 filter chain을 구성할 수 있다.
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
- 일반 Filter는 서블릿 컨테이너에 직접 등록하여 사용하는 필터이고 Security Filter는 DelegatingFilterProxy가 서블릿 컨테이너의 Filter에 등록되어 DelegatingFilterProxy가 Filter 작업을 Security FilterChain으로 위임하여 실행되는 필터.

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
  - 사용자가 메일이나 링크를 누르게 되면 Put, Delete와 같은 요청을 서버에 악의 요청을 보내는 것.
  - 서버에서는 요청 헤더의 referer에 등록되어 있는 요청 domain정보를 확인하여 올바른 domain에서 요청이 들어왔는지 확인하거나,
    Csrf-token을 사용해서 사용자가 요청시 csrf-token이 올바른지 판단하여 검증하는 방법

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

- 일반적인 Spring Security는 Security Context에 저장된 Authentication으로 세션을 별도의 스레드를 돌려 유지하기 때문에 유지비용이 들고 서버에서 관리하기 때문에 무겁습니다.
  하지만 JWT를 사용하게 되면 사용자의 정보는 서버 비밀키로 암호화되어 있어 정보가 안전하고 별도의 유지비용없이 인증 처리만 하면 되기 때문에 유지비용이 없고 가벼운 인증이 가능하기 때문입니다.

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
  Security Filter는 DelegatingFilterProxy를 서블릿 컨테이너 필터에 등록하여 일반 filter작업을 Security Filter Chain으로 위임받아UsernamePasswordAuthenticationFilter, SessionManagementFilter, ExceptionTranslationFilter 등이 차례로 실행됩니다.

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

- 인가 프로세스 후 생성되는 인증 객체인 Authentication은 principal, credentials, authority로 구성되어있으며 principal은 사용자의 식별 데이터, credentials은 암호, authority는 권한을 가지고 있습니다.
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
  - 가장 어려웠던 점 중 하나는 spring security에서 jwt를 적용하는데 개념과 구조에 대한 이해가 낮아 원하는 인증, 인가처리 프로세스로 구현하는 부분에서 제대로 적용시키지 못하여 많은 시간을 보냈었던것이 가장 힘들었던것 같습니다..

- 아쉬웠던점
  - 앱 서비스에 대한 서버였기때문에 spring security에서 지원하는 cors, crsf 등과 같은 보호 기능 등 해당 서비스에 사용되지 않기 때문에 security에서 제공하는 기능을 더많이 경험해보지 못한것과 데드라인에 맞춰 기능 구현에 급급해 이 기능이 왜 필요한지, 어디서 사용되는 건지 대한 기능의 활용성을 깊게 생각하지 못하면서 구현한것이 아쉬웠습니다.


</details>

-----------------------

<br>