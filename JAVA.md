# Java



<br>

-----------------------
### Java란

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------
+ Java
    + 자바는 객체지향 언어로써 정적타입을 지원해주고 객체지향의 특징을 사용하여 프로그램을 만드는 컴파일러 언어이자 인터프리터 언어이다.
    + JVM을 통해서 어떤 운영체제에 상관없이 독립적으로 동작한다.


</details>

-----------------------

<br>



<br>

-----------------------

### 컴파일 언어 vs 인터프리터 언어

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 컴파일 언어
  + 고급언어(코드)를 컴파일러를 통해 기계어로 번역하여 프로그램을 실행하는 언어
  + 장점
    + 번역된 코드를 실행만 시키면 되기 때문에 런타임 실행 속도가 빠르다.
  + 단점
    + 작성된 코드를 전체 번역하기 때문에 컴파일 시간이 오래걸린다.
+ 인터프리터 언어
  + 코드의 번역과 실행이 동시에 이루어지는 언어
  + 장점
    + 번역과 실행이 동시에 일어나기 때문에 수정 후 바로 실행가능하다.

  + 단점
    + 번역과 실행이 동시에 일어나기 때문에 실행속도가 느리다.

+ 자바는 컴파일 언어이자 인터프리터 언어
  + 자바는 자바코드를 자바 컴파일러(javac)를 통해 바이트코드로 변환(컴파일 언어 특징)하고 바이트코드가 JVM에 로드되어 인터프리터를 통해 바이트코드를 기계어로 번역(인터프리터 언어 특징)하여 명령을 수행한다.


</details>

-----------------------

<br>



<br>

-----------------------

### Java의 장단점

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 장점
  + 객체지향의 특징인 상속, 다형성, 캡슐화, 추상화 등의 특징을 지원한다.
  + 멀티 스레드 지원
  + JVM을 통해 어떤 운영체제에서도 독립적으로 동작한다.
  + JVM을 통해 메모리 관리와 최적화를 자동으로 해준다.

+ 단점
  + 컴파일 언어이기 때문에 컴파일시 시간이 오래걸린다.
  + 예외처리를 직접해주지 않는다면 컴파일이 되지 않는다.



</details>

-----------------------

<br>



<br>

-----------------------

### OOP(객체지향 프로그래밍) 특징

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ OOP란
  + 문제를 여러개의 객체 단위로 나누어 작업하는 방식으로, 객체들이 유기적으로 상호작용하는 프로그래밍 이론이다.

+ 상속(Inheritance)
  + 부모 클래스의 특징을 자식 클래스에게 물려주는것.
  + 부모 클래스의 기능을 이용하거나 확장하여 코드 재사용이 늘어나고 중복 코드 작성을 방지할 수 있다.

+ 다형성(Polymorphism)
  + 하나의 변수나 메소드가 여러 가지 타입을 가질 수 있는 것
  + 오버라이딩(Overriding) : 자식 클래스가 부모 클래스의 메소드를 입맛대로 변경해서 구현하는 것
  + 오버로딩(Overloading). : 같은 이름의 메소드를 사용해도 매개변수나 데이터 타입을 다른 형태로 재구성 하는 것.

+ 캡슐화(Encapsulation)
  + 객체가 하나의 목적을 위해 필드와 메소드를 하나의 캡슐로 묶은 것.
  + 정보은닉을 목적으로 접근제어자를 통해 캡슐화된 객체의 정보를 제어한다.
    + private : 해당 클래스에서만 접근 가능
    + default : 해당 패키지 내에서만 접근 가능
    + protected : 해당 패키지 내의 클래스와 해당 클래스를 상속받은 클래스에서만 접근 가능
    + public : 모든 곳에서 접근 가능

+ 추상화(Abstraction)
  + 객체의 공통적인 속성과 기능을 추출하여 정의하는 것.
  + 인터페이스 : 공통으로 구현해야하는 것을 정의하여 구현체에게 기능 구현을 강제하고 동일한 동작을 목적으로 한다.
  + 추상 클래스 : 추상메소드로 구현해야하는 것을 정의하고 일반 메소드로 기능(추상메소드 정의 기능x)을 구현하여 자식 클래스가 부모 클래스의 기능 사용과 확장을 목적으로 한다.



</details>

-----------------------

<br>



<br>

-----------------------

### 추상 클래스와 인터페이스의 차이

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 인터페이스는 구현을 강제하여 구현 클래스의 동일한 동작 수행을 보장하고 표준화를 유도하는 목적 (설계도).
  + able to : 무엇을 할 수 있는
  + 모든 지역변수는 public static final(상수)로 정의된다. (생략가능)
  + 모든 메서드는 public abstract(추상메서드)로 정의된다.
    + static method 사용가능
    + default method 사용가능 (구현 메서드)

  + 다중상속이 가능하다

+ 추상 클래스는 부모클래스의 특징을 상속받고 기능을 사용하며 확장을 목적.
  + kind of : 의 종류
    + 확장성
      + 상속의 목적은 재사용성과 확정성을 가지고 있다. 그리고 상속은 계층적이 아닌 확장적이다. (Father의 하위 클래스가 Dauther이 아닌것처럼, Dauther는 Father의 역할을 수행하지 못한다.)
      + 예를 들어 Bird의 한 종류인 펭귄은 Bird의 역할을 수행할 수 있다.
      + 즉, 확장이란 상속관계에서 구체화를 시켜가는 것이다. 그렇기 때문에 추상 클래스는 상속을 목적으로 자식 클래스로 구체화 시켜가는 과정이 있기 때문에 확장을 목적으로 하는것이고, 인터페이스 자체에서는 구현을 목적으로 하는것이지만 인터페이스간 상속이 가능하기 때문에 확장도 가능하다.

  + 추상 메서드를 정의할수있고, 일반 메서드를 구현할 수 있다.
  + 다중상속이 불가능하다.

+ 공통점
  + 정의된 기능(추상메서드)을 구현해야한다
  + new()를 통해 인스턴스를 생성할 수 없다.

+ 자바에서는 다중 상속의 모호성으로 인해서 상속은 하나밖에 되지않는다. 하지만 인터페이스는 여러개를 구현할 수 있다. 그렇기 때문에 인터페이스를 다중 상속의 문제점을 해결해주기 위한 것이라 생각할 수 있지만, 인터페이스와 추상 클래스의 존재 목적이 다르기 때문에 인터페이스를 다중 상속의 문제점을 해결하기 위한 것으로 사용하는 것은 옳지 못하다.

</details>

-----------------------

<br>



<br>

-----------------------

### OOP원칙 (SOLID)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 단일 책임 원칙(Single Responssibility Principle)
  + 클래스는 하나의 책임만 가져야 하며 그 책임은 캡슐화 되어있다. (캡슐화)

+ 개방 폐쇄 원칙(Open Closed Principle)
  + 클래스, 모듈, 함수 등의 소프트웨어 구성요소는 확장에 있어서 열려있어야하고, 변경에는 닫혀있어야한다.
  + 변경이 발생해도 기존 구성요소는 변경되지 않고 기존 구성요소를 확장해서 재사용할 수 있어야 한다. (추상화, 다형성)

+ 리스코프 치환 원칙(Liskov Substitution Principle)
  + 부모 클래스가 있던 자리에 자식 클래스로 치환해도 잘 구동되어야 한다. (상속)

+ 인터페이스 분리 원칙(Interface Segregation Principle)
  + 자신이 사용하지 않는 메소드에 의존관계를 맺어서는 안된다.
  + 큰 덩어리의 인터페이스보다 구체적이고 작은 단위로 나누어 필요한 메소드만 사용할 수 있게 해야한다.

+ 의존관계 역전 원칙(Dependency Inversion Principle)
  + 객체는 저수준 모듈보다 고수준 모듈에 의존해야한다.
    + 저수준 모듈 : 구현체
    + 고수준 모듈 : 인터페이스와 같은 객체 형태나 추상적 개념
    + <img width="400" alt="image" src="https://user-images.githubusercontent.com/57162257/193524894-221a4041-a80a-4e71-af70-d2c45ab47105.png">
  + 변화하기 쉬운것보다 변화하기 어려운것에 의존해야한다.
  + ex) 자동차는 변하기 쉬운 구체적인 타이어에 의존하면 안된다.
    + 타이어 종류에는 스노우타이어, 일반 타이어, 광폭타이어 등이 있어서 구체적인 타이어가 변경될 때마다 자동차에 영향을 준다.
    + 자동차는 구체적인 타이어가 아닌 추상화된 타이어에 의존하여 타이어가 변경되어도 자동차가 영향을 받지 않아야 한다.
    + <img width="426" alt="image" src="https://user-images.githubusercontent.com/57162257/185022337-b9fbcde6-c136-4dd5-bd01-2ee639b099a5.png">


</details>

-----------------------

<br>



<br>

-----------------------

### 객체지향 프로그래밍 vs 절차지향 프로그래밍 vs 함수형 프로그래밍

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 절차지향 프로그래밍 
  + 문제를 해결하기 위해 순차적으로 프로그래밍 하는 방법
  + 빠르게 구현할 수 있지만 절차가 정해져있기 때문에 유지보수가 어렵다.
+ 객체지향 프로그래밍
  + 구현하고자 하는 객체들의 상호작용을 프로그래밍 하는 방법
  + 상속, 다형성, 캡슐화, 추상화를 통해 결합도를 낮추고 응집도를 높일 수 있으며, 코드 재사용률을 높일 수 있다.
+ 함수형 프로그래밍
  + 문제를 해결하기 위해 함수를 정의하고 조합해서 해결하는 프로그램.
  + 순수함수들로 작성하여 모듈성이 증가하여 재사용률이 늘어나고, 메인코드의 가독성이 높아진다.
  + 순수함수를 통해 동시성 문제를 해결할 수 있다.
  + 순수함수
    + 입력값으로만 결과를 반환하는 함수
    + 동일한 입력값에는 동일한 출력값을 보장한다.
    + 함수 자체가 독립적이고 외부환경에 영향을 받지 않아 Thread-safe하여 병렬처리를 동기화 없이 사용가능
  + 1급객체
    + 변수나 데이터구조에 담을 수 있는 객체
      즉, 파라미터로 전달 할 수 있고, 반환값으로 전달할 수 있는 객체
    + 함수형 프로그래밍에서 함수를 1급객체 취급하기 때문에 함수를 유연하고 다양하게 사용가능.




</details>

-----------------------

<br>



<br>

-----------------------

### JDK

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ Java Development Kit의 약자로써 자바로 소프트웨어를 개발할 수 있는 여러 기능을 제공하는 키트

<img width="60%" alt="image" src="https://user-images.githubusercontent.com/57162257/181876371-48cb61ea-5568-436f-bb35-2db85782734e.png">


</details>

-----------------------

<br>

<br>

-----------------------

### JVM

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

- JRE
  - JVM은 `JRE`에 속해있는데 JRE는 `Java Runtime Enviroment`의 약자로 자바코드를 실행하기 위한 도구들로 구성된 패키지이다.
  - JDK에서 자바코드를 .jar로 압축 후 자바 컴파일러(javac)를 통해 바이트코드(.class)로 번역 한 후 JVM에 의해 기계어로 번역되어 명령을 수행한다.
- JVM 
  -  `Java Virtual Machine`의 약자로 자바코드에 대한 런타임 환경을 제공해주는 주체이다.
  - 자바는 운영체제에 상관없이 JVM에 의해 자바 프로그램이 실행된다.
  - 프로그램 메모리를 관리하고 최적화 해준다.

</details>

-----------------------

<br>



<br>

-----------------------

### JVM 구성

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

---

<img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/181876945-5a4f4397-d9de-4be4-a899-894d1bd436a1.png">

- Class Loader : 바이트코드를 JVM에 로드하고 Runtime Data Area에 링크
- Execution Engine
  - Interpreter : JVM에 로드된 바이트 코드를 기계어로 번역
  - JIT complier : 인터프리터가 번역했던 바이트코드를 저장해놨다가 중복되는 번역은 저장소에서 꺼내어 사용해서 인터프리터가 번역하는 시간을 줄여준다.
  - Garbage Collector : Runtime Data Area의 힙 메모리에서 참조되지 않는 객체를 삭제하여 메모리를 관리해주는 역할
- Runtime Data Area : 프로그램을 실행하기 위해 OS에서 할당받은 메모리 공간

</details>

-----------------------

<br>



<br>

-----------------------

### Java프로그램 실행 과정

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

1. 프로그램이 실행되면 JVM은 운영체제로 부터 메모리를 할당 받는다.
2. 자바 컴파일러(javac)가 자바코드(.java)를 바이트코드(.class)로 변환한다.
3. JVM의 Class Loader를 통해 바이트코드를 JVM에 로드하고 Runtime Data Area에 배치한다.
4. JVM의 Execution Engine에 의해서 Runtime Data Area에 있는 바이트코드를 기계어로 해석된다.
5. 명령이 수행된다.


</details>

-----------------------

<br>



<br>

-----------------------

### Runtime Data Area

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

<img width="60%" alt="image" src="https://user-images.githubusercontent.com/57162257/181877432-1707c1e7-d653-4385-92d2-f76a3b2dae71.png">

+ 프로그램을 실행하기 위해 운영체제에서 할당받은 메모리 공간
+ Thread
  + PC Register
    + 스레드가 생성될때 함께 생성되며 Thread가 어떤 부분을 명령으로 수행해야하는지를 저장하고 있다.
    + 즉, JVM의 명령 주소를 저장
    + 각 Thread는 메소드를 수행하고 PC는 해당 메소드의 몇번째 줄을 실행해야하는지 나타낸다.
  + JVM Stack
    + 매개변수, 지역변수, 반환 값 등 메소드의 정보를 저장했다가 메소드 종료시 삭제된다.
  + Nativ Metdho Stack
    + 자바 언어가 아닌 다른 언어가 있을때 저장
+ Heap
  + new() 로 생성된 객체 인스턴스들이 저장되는 메모리 영역
  + Young Generation과 Old Generation영역으로 나뉘어져 있다
    + Young Generation은 객체 생명주기가 짧은 젊은 객체들이 저장되는 영역으로 Eden과 survial 영역으로 나뉘어져있으며 Minor GC의 대상이다.
    + Old Generation은 객체 생명주기가 긴 오래된 객체들이 저장되는 영역으로 Major GC의 대상이다.
  + 모든 스레드가 공유
+ Method Area
  + 클래스, 메소드, static 변수 등을 저장하는 메모리 공간


</details>

-----------------------

<br>



<br>

-----------------------

### 가비지 컬렉션(Garbage Collection)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 사용되지 않는 Heap영역의 객체를 메모리 해제하여 메모리를 관리하는 역할
+ GC 종류
  + Serial GC : 하나의 스레드로 GC 수행
    + 적은 메모리와 적은 CPU코어에 적합
  + Parallel GC : java 8의 default GC, 여러 스레드로 GC 수행
    + 의도적으로 GC를 수행해야한다.
    + 애플리케이션과 GC가 병렬 수행
    + Age bit = 15
    + 다수의 스레드로 GC가 수행되기 때문에 메모리가 충분하고 코어가 많을때 사용
  + G1 GC : java 9의 default GC, Heap을 여러 영역으로 나누어 GC 수행
    - <img width="304" alt="image" src="https://user-images.githubusercontent.com/57162257/187113600-2594d63f-9214-4cf4-835e-814379d7f7fb.png">
    - young, old generation 영역을 명확하게 구분하는 전통적 heap과 다르게 eden, survivor, old, unused등의 작은 region으로 나누어져있다.
    - 이전에 사용하던 GC와 마찬가지로 최초 객체가 생성되면 Eden영역에 할당하고 이후 Survivor영역으로의 이동과 소멸, Old Generation으로 이동 생명주기를 가지게된다.
    - life cycle
      - ?
    - 장점 
      - young, old영역을 전체 탐색하는 것이 아닌, 특정 영역에 메모리가 많이 차있는 영역을 인식하여 GC를 수행함으로써 처리 속도가 빠르고 빠르게 빈 공간을 확보하기 때문에 GC의 빈도도 낮아진다.
    - 단점
      - Major, minor GC가 발생해도 공간이 부족한 경우 싱글 스레드로 Full GC(stop the world)가 발생하여 GC 처리 속도가 느리다.
+ Stop the World
  + GC를 실행하는 스레드를 제외한 스레드의 실행을 멈추어 JVM 애플리케이션 실행이 멈추는것.

+ GC 알고리즘
  + Reference Count
    + 객체를 참조하는 개수를 나타내는 reference count가 0이라면 GC의 대상이되는 알고리즘
    + 두 객체가 서로를 참조한다면 reference count가 영구적으로 1이되기 때문에 GC의 대상이 되지않는 문제가 발생할 수 있다.
  + Mark and Sweep
    + root space 에서 부터 그래프 순회하여 해당 객체에 접근가능한 객체는 `Mark`, 접근이 불가능한 객체는 GC의 대상이되어 삭제(`Sweep`)
      + 루트로 부터 연결된 객체 : Reachable
      + 연결되지 않은 객체 : UnReachable
      + 객체를 삭제하고 파편화를 막기위해 정리하는 것을 Compaction
      + root space : stack이나 static 공간에 선언된 변수들 즉, stack의 지역변수, method area의 static 변수, native method statck의 JNI참조
    + 의도적으로 GC를 실행시켜야한다, 애플리케이션 실행과 GC실행이 병행된다.
+ GC 동작과정
  1. Young Generation의 Eden영역이 포화상태가 된다.
  2. Mark and Sweep 실행(Minor GC)
  3. 살아남은 객체는 survival 0영역에 저장된다.
  4. survival 0영역이 포화되면 Minor GC 실행후  survival 1로 이동
  5. 살아남은 횟수 age가 일정 횟수가 된다면 Old Generation 영역에 저장된다.
  6. Old Generation이 포화상태가 되면 Major GC발생.
+ Reference Type
  + GC가 Reachable / UnRechable을 판단하는데 개발자가 컨트롤 할수 있게 해주는 type
  + Strong Reference
    + `Object obj = new Object()`
    + Thread stack이 직접적으로 Object에 접근 가능한 상태
    + null을 대입하지 않는 이상 gc대상으로 취급받지 않는다.

  + Weak Reference
    + `WeakReference<Object> weakReference = new WeakReference<>(new Object()) `
    + 항상 GC의 대상이 된다.

  + Phantom Reference
    + 올바르게 삭제하고 삭제 이후 작업을 조작하기 위한 타입
    + finalize 메소드에 의해 컨트롤할 수 있다.

+ 장단점
  + 장점 : 메모리 누수 방지, 해제된 메모리 접근 방지
  + 단점 : GC가 언제발생할지 모름
+ 주의 사항
  + Major GC는 Minor GC보다 실행시간이 훨씬 오래걸리며 GC실행시 발생하는 Stop the World로 인해 실시간 프로그램에서 크리티컬한 이슈가 발생할 수 있다.
  + old영역으로 넘어가는 객체 수를 줄이기 위해 String보다는 StringBuilder나 StringBuffer를 사용하고 로그 수를 줄인다. 그리고 Old영역의 크기를 조절해서 Major GC의 빈도를 줄이고 GC수행 시간을 적게 하도록 잘 조절한다.


</details>

-----------------------

<br>



<br>

-----------------------

### Char vs String

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ char 
  + 1개의 문자만 저장하는 타입

+ String
  + 문자열 주소를 저장하는 타입

+ char는 원시타입이기 때문에 동일성 비교(==)가 가능하지만 Character, String은 참조타입이기 때문에 동일성 비교시 참조 주소를 비교하기 때문에 같은 value를 비교하기 위해서는 동등성 비교(equals())를 해야한다.

</details>

-----------------------

<br>



<br>

-----------------------

### 동일성 비교(==) vs 동등성 비교(equals())

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 객체일 경우 동일성 비교는 참조 주소를 비교하고 동등성 비교는 객체의 value를 비교

</details>

-----------------------

<br>



<br>

-----------------------

### String vs StringBuilder vs StringBuffer

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ String
  + <img width="50%" alt="image" src="https://user-images.githubusercontent.com/57162257/181692343-8d8792b1-09dd-40d1-ba6f-7460e64c84bc.png">
  + String 선언은 ""선언과 new String() 선언이 있다.
  + ""선언은 리터 선언이며 Heap의 String Pool에 저장이되며 같은 value일 때 동일성 비교가 가능하다.
    + 리터럴(literal) : 데이터 그 자체, 변수에 넣는 변하지 않는 데이터
  + new String()선언은 Heap의 Eden에 저장되며 같은 value라도 다른 참조 주소를 가지기때문에 동등성 비교를 해야한다.
  + 문자열 연산시 새로운 객체가 생성되어 저장되기 때문에 Heap메모리 관리에 치명적일수 있다.
  
+ StringBuilder
  + StringBuilder는 new StringBuilder()로 선언하며 문자열 연산시 StringBuilder의 객체의 크기가 변할 뿐 새로운 객체가 생성되지 않아 메모리관리에 효율적이다.
  + 비동기화 처리

+ StringBuffer
  + StringBuilder와 마찬가지로 문자열 연산시 객체의 크기가 변할 뿐 새로운 객체가 생성되지 않아 메모리 관리에 효율적이다.
  + 동기화 처리



</details>

-----------------------

<br>



<br>

-----------------------

### String 불변성

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

+ 불변 개체란 생성된 후에도 내부 상태가 일정하게 유지되는 개체
+ String은 변수에 할당되면 참조를 업데이트하거나 내부 상태를 어떠한 상태로 변경할 수 없다.
+ 성능
  + 문자열 리터럴을 string pool에 등록했을때 동일한 문자열을 새로 생성하는 것이 아닌 string pool에서 찾아 가져와 메모리 효율성을 높일 수 있다.
  + 만약 immutable이 아닌 mutable이라면 string pool에 저장된 데이터가 변경되면 해당 heap영역의 데이터를 참조하는 변수들의 값도 변경된다.

+ 동기화
  + 멀티 스레드 환경에서 String 여러 스레드에서 공유될 수 있는데, immutable하기 때문에 참조 값이 변경되는 것이 아닌 새로운 데이터를 생성하여 참조하기 때문에 멀티 스레드 환경에서도 thread-safe하게 사용할 수 있다.

+ 해시코드 캐싱
  + String에서 해시코드는 참조 데이터를 한번만 해시코드로 변경하고 해시를 재사용한다.
  + 그렇기 때문에 참조 데이터가 변경된다면 해시코드에 문제가 생길수 있다.
  + 따라서 문자열로 해시 구현을 사용하는 컬렉션의 성능이 좋다.

+ 보안
  + 특정 문자열에 대해서 보안 검사를 수행했을 때 만약 mutable하다면 다른 곳에서 참조 데이터를 변경할 수 있기 때문에 문제가 발생할 수 있다.


</details>

-----------------------

<br>



<br>

-----------------------

### 데이터 타입

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 원시 타입(Primitive type) : 크기가 작고 고정적이기 때문에 Stack메모리에 저장
  + 논리형 : boolean (1bit)
  + 문자형 : char (2bit)
  + 정수형 : byte (8bit), int (32bit), long (64bit)
  + 실수형 : float (32bit), double (64bit)

+ 참조 타입(Reference type)
  + 크기가 가변적이고 동적이다.
  + 데이터는 Heap메모리에서 관리되고 참조 주소는 Stack메모리에서 관리된다.
  + 더 이상 참조되지 않으면 GC 삭제 대상이 된다.
  + value를 필요로 할때마다 언박상 과정을 거치게 되어 접근속도가 느려진다.



</details>

-----------------------

<br>



<br>

-----------------------

### 제네릭(Generic)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 클래스나 메소드를 사용할때 데이터 타입을 외부에서 설정하는 것

+ 제네릭이 없을 때는 여러 타입을 사용하는 클래스나 메소드에서 인수나 반환값을 Object타입으로 사용했다. 이는 객체를 꺼낼때 타입 변환을 직접 해주어야 했고 오류가 발생할 가능성이 존재한다.

+ 제네릭을 사용함으로써 컴파일 시에 미리 타입이 정해지고, 타입 변환과 같은 번거로운 작업을 생략할 수 있게 되었다.

+ 컴파일 시점에 타입을 체크함으로서 코드의 안정성을 높여주는 기술

  + List< T > 에서 T가 타입 매개변수
  + 장점
    + 컴파일 시점에 강력한 타입 검사
      + 선언한 타입 이외의 타입이 들어오게 되면 컴파일 에러 발생
    + 캐스팅 (타입 변환) 제거
      + 제네릭 타입을 사용하지 않게되면 Object로 데이터를 가져와 형 변환 과정이 추가되어야한다.

+ 종류

  + 타입파라미터 T
  + 와일드카드 ?

+ 공변과 불공변

  + 공변
    + A가 B의 하위 타입일때 배열 A[]은 배열 B[]의 하위 타입이다.

  + 불공변
    + A가 B의 하위 타입일때 List< A >는 List< B >의 하위 타입이 아니다.
    + 제네릭 타입은 불공변이다.

+ 제네릭 클래스와 제네릭 메소드

  + ```java
    class MyParent<T>{	//제네릭 클래스 타입
      private T t;
      public void set(T t){
        this.t = t;
      }
      public T get(){
        return this.t;
      }
      
      public <T> printElement(T t){	//제네릭 메소드 타입
        System.out.println("제네릭 클래스 타입 : "+this.t.getClass().getName());
        System.out.println("제네릭 메소드 타입 : "+t.getClass().getName());
      }
    }
    ```

+ 와일드 카드

  + 모든 타입을 대신할 수 있는 타입
  + 정해지지 않은 unknown type이기 때문에 Collection<?>로 선언시 모든 타입에 대해 호출이 가능해졌다.
    + 특정 타입이 지정되지 않았으므로 Object로 받아야한다.

+ 한정적 와일드 카드

  + 정해지지 않은 타입으로 발생하는 문제를 해결하기 위해 특정 타입을 기준으로 상한 범위와 하한 범위를 지정해준다.
  + 상한 경계 와일드 카드
    + extends를 이용해 와일드카드의 최상위 타입을 정의하여 상한 경계를 설정한다.
    + <? extends MyParent>로 선언해줌으로서 선언한 타입의 자신과 자신의 자식 클래스가 가능해진다.
    + <? extends MyParent>로 선언한 타입은 MyParent로 객체를 꺼낼수 있다.
      + 해당 선언은 최소 MyParent의 자식 클래스가 확실하기 때문이다.

    + 하지만 객체는 저장할 수 없다.
      + <? extends MyParent>로 선언된 타입에 자식 클래스가 저장되게 된다면 자식 클래스는 부모 클래스가 될수 있지만, 부모 클래스는 자식 클래스가 될수 없기 때문에 타입을 명확히 지정해줄 수 없기 때문이다.

  + 하한 경계 와일드 카드
    + 상한 경계와 반대로 super를 이용해 와일드카드의 최하위 타입을 정의하여 하한 경계를 설정한다.
    + <? super MyParent>로 선언해줌으로서 선언한 타입의 자신과 부모 클래스가 가능해진다.
    + <? super MyParent>로 선언한 타입은 MyParent와 자식 클래스 타입을 저장할 수 있다.
      + 해당 선언은 최소 MyParent클래스가 확실하기 때문에 자기 자신인 MyParent와 MyParent가 될 수 있는 그 자식 클래스들이 저장될 수 있기 때문이다.

    + 하지만 객체를 꺼낼수 없다.
      + <? super MyParent>로 선언된 타입에는 MyParent와 MyParent의 부모 클래스 타입이 저장되어 있을 수 있는데, MyParent의 부모클래스(Object 등..)은 MyParent와 그 자식 클래스가 될 수 없기 때문이다.
      + 하지만 <? super MyParent>에는 MyParent와 그 부모 클래스타입이 들어있을 수 있기 때문에 최상위 타입인 Object로는 읽어오기가 가능하다.

+ PECS

  + Producer-Extends, Consumer-Super

  + 언제 상한경계를 사용하고 하한경계를 사용해야하는지에 대한 공식.

  + ```java
    void printCollection(Collection<? extends MyParent> c){	//와일드카드 타입 생성
      for(MyParent e : c){
        System.out.println(e);
      }
    }
    
    void addElement(Collection<? super MyParent> c){	//와일드카드 타입 소비
      c.add(new MyParent());
    }
    ```

  + Collection에서 객체를 꺼내오면 와일드카드 타입의 객체를 생성(producer)하기 때문에 extends를 사용해준다.

  + Collection에 객체를 저장하면 와일드카드 타입의 객체를 소비(consume)하기 때문에 super를 사용해준다.



</details>

-----------------------

<br>



<br>

### Call By Value vs Call By Reference

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ call by value
  + 함수 호출시 인자로 전달되는 값을 복사하여 전달되기 때문에 함수 내부에서 인자 값이 변경되어도 외부에서는 영향을 받지 않아 값이 변경되지 않는다.

+ call by reference
  + 함수 호출시 인자로 전달되는 변수의 주소를 전달하기 때문에 함수 내부에서 인자 값이 변경되면 외부에서 영향을 받아 값이 변경된다.
+ java는 call by value
  + <img width="60%" alt="image" src="https://user-images.githubusercontent.com/57162257/181691033-9553a6ef-09d2-4844-bfd4-ab9e16695d8e.png">
  + java는 함수 호출시 인자로 전달되는 변수의 주소를 복사하여 전달한다. 그렇기 때문에 인자의 주소를 변경하더라도 복사된 주소이기 때문에 외부 변수에 영향을 주지 않아 변경이되지 않는다.
  + 하지만 복사한 주소도 Heap영역의 동일한 데이터를 참조하고 있기 때문에 인자의 value를 변경한다면 외부 변수의 value는 영향을 받아 value가 변경된다.
  + 즉, 인자의 value를 변경하면 외부 변수의 value도 변경되어 call by reference로 착각할 수 있지만, 인자는 복사된 주소이기 때문에 결국은 call by value이다.



</details>

-----------------------

<br>



<br>

-----------------------

### 직렬화(Serialization)

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 자바 내부에서 사용하는 객체 또는 데이터를 외부 자바 시스템에서 사용할 수 있도록 `바이트 형태`로 변환하는 기술 (JVM에 저장된 객체, 데이터 -> 바이트 형태로 변환)
+ 직렬화를 사용하는 이유
  + 원시 타입의 경우 크기가 고정적이기 때문에 바이트 단위 변환에 문제가 없지만, 객체인 경우 크기가 가변적이기 때문에 객체를 바이트 형태로 변환하기 위해서 별도의 변환 과정이 필요하기 때문이다.

+ 방법
  + 직렬화하려는 객체를 Serializable 인터페이스를 상속받고 ObjectOutputStream을 이용하여 직렬화를 진행한다.

+ **역직렬화(Deserialization)**
  + 바이트 형태의 데이터를 Object나 데이터로 변환하는 기술
  + 직렬화한 대상 객체는 동일한 `serialVersionUID`를 가져야한다.
  + 방법
    + ObjectInputStream을 통해 역직렬화를 진행
    + 가져온 ObjectInputStream의 readObject()를 통해 역직렬화한 객체를 가져온다.

  + 주의사항
    + 역직렬화를 하기 위해서는 직렬화한 객체와 동일한 serialVersionUID와 동일한 객체가 필요하다.
    + serailVersionUID가 같아도 객체의 필드 개수가 다르다면 다른 객체로 인식하여 역직렬화가 불가능하다.
    + 동일한 객체여도 serialVersionUID가 다르면 다른 객체로 인식하여 역직렬화가 불가능하다.
      + 동일한 객체면 별도의 설정이 없다면 자바에서 같은 serialVersionUID로 설정한다.

+ Transient
  + 객체에 Transient예약어를 선언한 변수는 Serializable 대상에서 제외되어 역직렬화 했을때 존재하지 않는 값으로 나타난다.
  + 이는 보안상이나 필요없는 데이터를 직렬화하지 않을때 사용하는 예약어이다.

+ 사용시기
  + 서블릿 세션 : 세션을 서블릿 메모리상에서 운용한다면 직렬화가 필요없지만, 파일로 저장하거나 세션 클러스터링 등을 이용할때 직렬화를 통해 저장되어 전달된다.
  + 캐시 : Redis, memcached 라이브러리에서 사용된다.



</details>

-----------------------

<br>



<br>

-----------------------

### Java Reflection

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

+ 구체적인 클래스 타입을 알지 못하여도 해당 클래스의 정보(메서드, 생성자, 필드 등)에 접근할 수 있게 하는 API
+ 자바는 컴파일 시점에 타입을 결정하게 되는데, 클래스의 타입을 알지 못한다면 Object타입으로 선언해주게 되는데 이렇게 되면 Object타입의 정보만 사용할 수 있다.
  Java의 reflection을 사용하게 된다면 클래스 타입을 알지 못하여도 클래스 이름만으로 클래스 정보에 접근할 수 있고 수정할 수 있다.
+ 동작원리
  + Java코드는 JVM에 로드되면 Method Area에 저장되게 된다. 이를 이용하여 Reflection은 클래스 이름을 통해 Method Area영역에 있는 클래스를 탐색하여 클래스 정보를 가져올 수 있다.

+ 장점과 단점
  + 장점
    + 프레임워크와 라이브러리에서 사용자정의 클래스를 사용할 수 있다.
    + 디버거가 private정보에 접근하여 검사할 수 있다.

  + 단점
    + 컴파일 시점이 아닌 런타임 시점에 타입을 분석하기 때문에 성능 오버헤드가 발생할 수 있다.
    + private정보에 접근할수 있기 때문에 내부정보가 노출될 수 있다.

+ 사용
  + BeanFactory
    + 스프링 컨테이너에서 빈을 등록하고 사용하게 해주는 BeanFactory는 런타임 시점에 빈으로 등록될 클래스를 탐색하고 인스턴스를 생성하여 빈으로 등록해주게 된다.
      이때 Reflection을 이용하여 인스턴스를 생성하여 빈으로 등록해준다.

  + JPA
    + JPA는 Entity를 자동으로 생성할때, Reflection을 사용한다. 이때 Entity를 선언할때 기본 생성자가 필수로 선언되야하는데, 이는 Reflection이 가져올수 없는 정보 중 하나가 생성자의 인자값이다. 그렇기 때문에 기본 생성자를 생성하고 클래스의 정보를 가져와 인스턴스를 생성하기 때문에 Entity선언시 기본 생성자가 필수로 선언되야한다.



</details>

-----------------------

<br>



<br>

-----------------------

### Java Collection

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

<img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/181880446-bea276d3-7c23-472a-9fc7-3d9946d27b25.png">

여러 원소를 담을 수 있는 자료구조로 Set과 List는 Collection을 상속하고 Map은 Collection 프레임워크에서 Collection과 별도로 정의되어있는 인터페이스

Collection Framework : 여러 원소를 저장하기 위한 프레임워크

Collection : 연속되는 데이터를 저장하기 위한 인터페이스

Collections : 객체를 다루기 위한 Objects 클래스, Collection 프레임워크와 밀접하게 동작하며 sort와 같은 기능을 제공해 Collection등의 자료구조를 다룰수 있게 도와주는 클래스

- List : 데이터의 중복을 허용하고 순서를 보장하는 자료구조 (인터페이스)
  - ArrayList
    - 데이터의 크기가 정해져있지 않아 List의 크기가 가변적으로 변하는 자료구조
    - 인덱스가 있어 탐색은 빠르지만 삽입,삭제는 느리다.
  - LinkedList
    - 각각의 노드를 연결한 자료구조
    - 노드가 연결되어있어 삽입,삭제는 빠르지만 인덱스가 없어 탐색은 느리다.
  - Vector
    - ArrayList와 동일한 동작을 가진다.
    - 동기화
    - Vector는 크기가 증가할 때 100%증가하지만, ArrayList는 50%씩 증가한다.
- Set : 데이터의 중복을 허용하지 않고 순서를 보장하지 않는 자료구조 (인터페이스)
  - HashSet
    - 데이터를 저장할 때 해시코드를 이용해 중복되는 해시코드 여부를 파악하고 없다면 데이터를 저장한다.
    - 비동기화
  - LinkedHashSet
    - HashSet과 동일한 동작을 한다.
    - 순서 보장
    - 비동기화
  - TreeSet
    - HashSet과 동일한 동작을 한다.
    - 오름차순 정렬 보장하기 때문에 직접 정의한 객체라면 Comparator를 구현하여 정렬 방법을 지정해줘야한다.
    - 비동기화
- Map : 데이터를 저장할때 key, value 형태로 저장하고 key의 중복을 허용하지 않는 자료구조 (인터페이스)
  - HashMap
    - 데이터를 저장할 때 key와 value를 선언하여 저장하며 key의 중복을 허용하지 않는다.
    - 내부 해시코드에 따라 키 순서가 정해지기 때문에 순서를 보장하지 않는다.
    - key와 value의 null을 허용한다.
    - 비동기
  - LinkedHashMap
    - HashMap과 동일한 동작을 한다.
    - 순서 보장
    - key와 value의 null을 허용한다.
  - TreeMap
    - 내부적으로 레드-블랙 트리로 저장된다.
    - key의 오름차순 정렬을 보장하기 때문에 직접 정의한 객체인 key라면 Comparator를 구현하여 정렬 방법을 지정해줘야한다.
    - key와 value의 null을 비허용한다.
  - HashTable
    - HashMap과 동일한 동작을 한다.
    - key와 value의 null을 비허용한다.
    - 객체 자체에 락을 걸어준다 (synchronized), 읽기쓰기 작업 모두 동기화
  - ConcurrentHashMap
    - HashMap과 동일한 동작을 한다.
    - key와 value의 null을 비허용한다.
    - 조작하는 item에 대해 쓰기 작업에만 락을 걸어준다 (synchronized block)

</details>

-----------------------

<br>



<br>

-----------------------

### HashTable과  ConcurrentHashMap

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

+ 공통점
  + Key, value 형태로 저장되며 key, value의 null을 허용하지 않으며 동기화 기능을 제공한다.

+ 차이점
  + HashTable
    + HashTable에서의 모든 기능에 synchronized 처리 되어 해당 객체가 동기화 처리된다.

  + ConcurrentHashMap
    + 어떤 아이템을 조작(쓰기)할때 해당 아이템에만 락만 걸기 때문에 멀티 스레드 환경에서 HashTable보다 효율이 좋다.



</details>

-----------------------

<br>



<br>

-----------------------

### 클래스, 객체, 인스턴스

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

+ 객체 : 자신의 고유 특성을 가지는 물리적, 추상적 대상
+ 클래스 : 객체의 특성 및 기능을 정의한 설계도
+ 인스턴스 : 클래스로 생성된 객체 하나하나


</details>

-----------------------

<br>





<br>

-----------------------

### Java 8

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

+ Stream
+ Optional
+ 함수형인터페이스
+ 람다 표현식
+ Java8을 사용하는 이유
  + Java8은 외부 개발 툴과 연결에 있어서 안정성이 보장되어있고 많은 기능들이 추가되었지만, 개발에있어서 큰 차이를 느끼지 못했기 때문에 안정성이 보장되어있는 java8 선택



</details>

-----------------------

<br>





<br>

-----------------------

### Stream API

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ Java 8에 등장한 기술로 반복 요소 계산 처리 기능을 제공하는 API
+ 특징
  + Parallel 메소드를 제공해서 병렬처리가 가능하다 (내부적으로 스레드풀을 만들어 병렬 처리)
    + parallelStream()은 thread-safe하지않아 별도의 처리가 필요하다.
    + Fork-join을 사용해서 하나의 쓰레드를 재귀적으로 특정 depth까지 반복하여 여러 쓰레드로 나누고 자식 스레드의 결과 값을 취합하여 최종스레드의 결과를 만들어 리턴하는 방식.
    + Fork-join을 사용해서 각 스레드가 공평하게 작업을 처리한다.
    + pararllel은 공유된 thread pool을 사용하기 때문에 성능장애를 일으킬 수 있다.
  + 불변성(Immutable)이기때문에 원본 데이터를 읽기만 할 뿐 변경하지 않는다.
    + 데이터를 변경할 수 없으며 변경하기 위해서는 재할당을 해야한다.
  + 내부반복으로 작업을 수행하며 최종 연산 후 stream이 닫히므로 일회성 API이다.



</details>

-----------------------

<br>



<br>

-----------------------

### Collection과 Stream

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 계산시점
  + Collection : Collection은 데이터를 메모리에 저장하는 자료구조이므로 Collection에 저장되어있는 요소는 계산이 완료되어 있어야 한다.
  + Stream : stream()을 호출하는 시점부터 요소를 계산한다.

+ 반복
  + Collection : 저장되어있는 요소는 계산이 완료되어 있어야하기 때문에 외부에서 반복하여 저장된다. (외부 반복)
  + Stream : 내부에서 중간연산, 최종 연산등으로 반복하여 저장한다. (내부 반복)



</details>

-----------------------

<br>



<br>

-----------------------

### Lazy Evaluation

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ Stream의 내부연산은 작업을 바로 실행하는 것이 아니라 마지막에 어떤 연산을 필요로 하는지 판단 후 연산 작업을 수행한다.
+ 즉, 내부 연산시 최종 연산자를 판단하고 불필요한 반복작업을 수행하지 않고 종료하는 것.
+ stream에서 제공하는 최종 연산자
  + limit() : 연산 사이즈 제어
  + findFirst() : 연산 결과의 첫번째 요소를 반환 후 종료
  + findAny() : 병렬연산하여 아무값 반환 후 종료
    + parallel 사용
  + anyMatch() : stream 요소 중 조건이 true인 요소가 있다면 종료
  + allMatch() : stream 요소 중 조건이 하나라도 false인 요소가 있다면 종료
  + nonMatch() : stream 요소 중 조건이 하나라도 true인 요소가 있다면 종료



</details>

-----------------------

<br>



<br>

-----------------------

### Wrapper Class

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 기본 타입인 데이터를 객체로 감싸주는 클래스로, 기본타입 데이터를 Wrapper Class 인스턴스의 value로 저장.
+ 동등성 비교를 통해 value를 비교해야 한다.
+ 사용 이유
  + null값을 사용하기 위해
  + 제네릭 타입을 사용하기 위해
  + Collection에서 객체를 사용하기때문이다.
  + 멀티 스레드에서 동기화 처리를 위해 객체가 필요하다.



</details>

-----------------------

<br>



<br>

-----------------------

### 박싱 & 언박싱

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 박싱 : 기본 타입(char, int ...)을 wrapper class의 인스턴스로 변경하는 과정

+ 언박싱 : wrapper class의 인스턴스에 저장된 value를 기본 타입으로 꺼내는 과정

+ Integer boxing과 unboxing

  + `Integer i = 127`은 컴파일 단계에서 `Integer i = Integer.valueOf(127)`을 수행한다. (Auto boxing)

    + Integer.valueOf()를 사용하여 박싱을 할 경우 -128~127은 동등성 비교가 보장이 된다.

    + Integer내부의 IntegerCache에는 -128~127까지의 Integer가 저장되어있어 해당 범위의 숫자를 사용하게되면 Cache에서 object를 가져와 반환해주기 때문에 동등성 비교가 보장된다.

      + -128~127은 실제 개발에서 많이 사용되는 값이기 때문에 캐시를 해놓는다고 한다.

    + ```java
      Integer integer1 = 127;
      Integer integer2 = 127;
      
      System.print(integer1 == integer2); //true
      
      Integer integer3 = 128;
      Integer integer4 = 128;
      
      System.print(integer3 == integer4); //false
      ```

  + `Int c = i`은 컴파일 단계에서 `int c = i.intValue()`을 수행한다. (Auto unboxing)



</details>

-----------------------

<br>



<br>

-----------------------

### Optional

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 값의 존재여부를 표현하는 클래스
+ 함수
  + orElse : 값의 null여부와 상관없이 호출
  + orElseGet : 값이 null인경우 호출



</details>

-----------------------

<br>



<br>

-----------------------

### 함수형 인터페이스

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 구현해야할 추상 메소드 하나만 정의된 인터페이스로써 Java 8에 등장.
+ `@FunctionalInterface` 어노테이션을 통해 객체 선언 및 오버라이딩 필요없이 람다식을 통해 코드를 간결하게 작성하는 것이 가능하다.
+ 사용
  + Collections.sort( [List타입] , [`Comparator 함수형 인터페이스`])
  + PriorityQueue<>( [`Comparator 함수형 인터페이스`] )
  + Stream().map(( [`Function 함수형 인터페이스`] ))
  + mapToInt( [`ToIntFunction 함수형 인터페이스`] )


<img width="527" alt="image" src="https://user-images.githubusercontent.com/57162257/181903333-5a02e0ee-c515-4eb0-a6be-4cee1cf7da2f.png">


</details>

-----------------------

<br>



<br>

-----------------------

### 람다 표현식

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 익명의 함수를 단순한 문법으로 나타내는 표현식으로써 Java 8에 등장.
+ 구현해야할 하나의 추상 메소드만 정의되어있는 함수형 인터페이스에 사용가능.
+ 병렬작업에 효율적이다.


</details>

-----------------------

<br>



<br>

-----------------------

### Java 11

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ default GC가 parallel GC에서 G1 GC로 변경되었다.
+ String 메소드 추가
  + isBlank() : 문자열이 비어있거나 공백일 때 true
  + strip : 문자열 앞 뒤의 공백 제거
    + Java 8에는 trim이라는 공백 제거 함수가 있는데 \u200이하의 공백 문자만 제거해줄수있지만 java 11의 strip은 더 많은 공백문자열을 제거해줄 수 있다.
  + repeat(n) : 문자열을 n번 반복하여 반환
+ Collection의 toArray()메소드를 오버로딩하는 것이 추가되어 IntFunction이 추가되어 원하는 타입의 배열을 선택하여 반환. (String[]::new 와 같은 선언이 가능해짐)
  + <img width="514" alt="image" src="https://user-images.githubusercontent.com/57162257/181903621-6b0527b5-cddf-4fd7-b6e0-46202a0bd9ac.png">
  + <img width="509" alt="image" src="https://user-images.githubusercontent.com/57162257/196023875-252c1fdb-d499-4adb-b864-f6b78eb57adf.png">
  + Java 8에서는 list.toArray(new String[0])으로 변경해주는데 파라미터로 넘겨주는 0은 만들 배열의 크기이다. 만약 list의 크기보다 넘겨주는 값이 더 크다면 반환되는 배열의 남은 공간에는 null로 나오게 된다.
+ 람다 표현식에서 지역변수에 var 사용이 가능해져 컴파일 시 타입을 추론하게 하고 타입에 사용할수 있는 어노테이션을 사용할 수 있다..
  + <img width="561" alt="image" src="https://user-images.githubusercontent.com/57162257/181903638-846ceb6c-6dc8-4294-bcc9-519a7b696492.png">

</details>

-----------------------

<br>



<br>

-----------------------

### Java 동기화

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ synchronized

  + synchronized

    + 일반 메소드에 synchronized 선언 시, 해당 객체(this)에 lock이 걸리기 때문에 같은 객체를 여러 스레드가 사용한다면 병목 현상이 발생할 수 있다.

      ```java
      class synchronized{
        private int shareSource;
        
        public synchronized checkSyn(int source){
            if(shareSource != source) System.out.println("동기화 실패");	//동기화 처리 (로그 x)
        }
      }
      ```

    + 만약 위 코드에서 synchronized를 제거한다면 "동기화 실패" 로그가 발생한다.

  + synchronized block

    + 메소드에 synchronized 선언 시 해당 객체에 lock이 걸리지만 synchronized block을 사용한다면 객체가 아닌 해당 메소드에서만 lock이 걸리게 된다. (필요한 부분만 동기화)

      ```java
      class synchronized{
        private int shareSource;
        
        public checkSyn(int source){
      		synchronized(this){
            if(shareSource != source) System.out.println("동기화 실패");	//동기화 처리 (로그 x)
          }
        }
      }
      ```

    + synchronized block시 인자(객체 참조 표현식)에 this로 걸어주게 되면 this를 인자로 가진 synchronized block은 모두 lock이 걸리게 된다. 만약 synchronized block별로 lock을 걸어줄 메소드를 지정해주려면 Object1, Object2 등의 별도로 선언한 객체로 동기화 처리를 할 synchronized block의 인자로 정의하게 되면 object1으로 정의한 메소드끼리 동기화가되고 object2로 정의한 메소드끼리 동기화가 된다.

      ```java
      class synchronized{
      	private final List<Integer> list1 = new ArrayList<>();
        private final List<Integer> list2 = new ArrayList<>();
        
        private final Object object1 = new Object();
        private final Object objcet2 = new Object();
        
        /// object1 끼리 동기화
        
        public void addList1(int source){
          synchronized(object1){
            list1.add(source);
          }
        }
        
        public int getList1(int index){
          synchronized(object1){
            return list1.get(index);
          }
        }
        
        ///
        /// object2 끼리 동기화
        
        public void addList2(int source){
          synchronized(object2){
            list2.add(source);
          }
        }
        
        public int getList2(int index){
          synchronized(object2){
            return list2.get(index);
          }
        }
        ///
      }
      ```

  + singletone synchronized

    + 싱글톤은 하나의 객체를 여러 스레드가 공유하는 디자인 패턴이므로 하나의 객체를 생성하여 여러 스레드가 사용하는 것과 같은 동기화 문제가 발생할 수 있다.

  + static method synchronized

    + static method에 synchronized를 선언하면 해당 class에 lock을 걸어주기 때문에 해당 클래스의 객체를 사용하는 스레드는 병목 현상이 발생할 수 있다.

      ```java
      class synchronized{
        private int shareSource;
        
        public static synchronized checkSyn(int source){
           if(shareSource != source) System.out.println("동기화 실패");	//동기화 처리 (로그 x)
        }
      }
      ```

  + static method synchronized와 method synchronized 혼용

    + static method의 synchronized는 class에 lock을 걸어주고 일반 method의 synchronized는 해당 객체(this)에 lock을 걸어준다. 그렇기 때문에 static method의 synchronized는 동기화 처리가 되어 class에서 공유하는 자원에 대해 동기화 처리가 잘 되지만 일반 method는 해당 객체(this)에 lock을 걸어주기 때문에 class에서 공유하는 자원에 대해 동기화가 깨지게 된다.

      ```java
      class synchronized{
        private int shareSource;
        
        public static synchronized checkStaticMethodSyn(int source){
          if(shareSource != source) System.out.println("동기화 실패");	//동기화 깨짐 (로그 o)
        }
        
        public synchronized checkMethodSyn(int source){
          if(shareSource != source) System.out.println("동기화 실패");	//동기화 깨짐 (로그 o)
        }
      }
      ```

    + 즉, static method synchronized와 일반 method synchronized를 함께 사용할때 static method간에서는 동기화 처리가 되지만, 일반 method synchronzied에서 동기화를 깨버리기 때문에 결과적으로 동기화 처리가 되지 않는다.

+ volatile : 키워드가 선언된 자원은 하나의 스레드만 write하고 나머지 스레드는 read만 한다는 전제 하에 동시성 부여

+ atomic : 여러 스레드에서 wirte를 해도 동시성 문제가 발생하지 않는다. Synchronized 보다 적은 비용으로 동시성 보장.


</details>

-----------------------

<br>



<br>

-----------------------

### Java 멀티 스레드 프로그래밍

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 멀티스레딩을 수행할 클래스는 Thread 클래스를 상속받아 run() 함수를 오버라이딩하여 로직을 수행한다.
  + 장점 : Thread 클래스의 기능을 사용할 수 있다.
  + 단점 : 다중 상속이 불가능 하다.
+ 멀티스레딩을 수행할 클래스는 Runnable 인터페이스를 상속받아 run()을 구현하여 Thread 생성자의 인수로 넘긴다.
  + 장점 : 재사용성이 높고 다른 클래스 상속이 가능하다.
  + 단점 : Thread클래스의 함수를 사용할 수 없다.
+ ExecutorService
  + ExecutorService는 자바에서 스레드 풀을 이용하여 멀티스레드를 쉽게 사용할수있도록 도와주는 인터페이스
  + execut(), submit()과 같은 메서드로 Runnable, Callable을 실행시켜준다.
    + Callable인터페이스는 내부적으로 실행한 결과를 반환해줄 수 있다.




</details>

-----------------------

<br>



<br>

-----------------------

### Error & Exception

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

+ <img width="600" alt="image" src="https://user-images.githubusercontent.com/57162257/187188855-0ee27b26-7458-48d4-a77c-1c0851779910.png">
+ Error
  + 시스템에 비정상적인 상황이 발생한 경우
  + 런타임 시에 발생하며 예측이 불가능하고 처리할 수 없다.
  + 종류 : StackOverFlow, OutOfMemory

+ Exception
  + 입력받은 데이터 처리가 불가능하거나 잘못된 참조가 발생한 경우
  + Checked Exception
    + RuntimeException을 상속받지 않는 Exception으로, 컴파일 시점에 발생하고 반드시 예외를 처리해주어야하는 예외
    + 종류 : IOException, SQLException

  + UnChecked Exception
    + RuntimeException을 상속받는 Exception으로, 런타임 시점에 발생하고 명시적으로 예외처리를 하지 않아도 되는 예외
    + 종류 : NullPointException, IndexOutBoundException

  + spring에서의 트랜잭션 처리 설정 중 RuntimeException시 롤백을 수행하는 옵션이 있어서 UnCheckedException에서는 롤백이 수행된다고 오해를 하지만, 어떤 예외든 개발자가 필요에 따라 예외처리를 해주고 특정 기술을 제어하는 것이다.


</details>

-----------------------

<br>



<br>

-----------------------

### final vs finally vs finalize

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ final : 변수, 함수, 클래스가 변경 불가능 하도록 만든다.
  + 기본 타입 : 해당 변수의 값이 변경되지 못한다.
  + 참조 타입 : 해당 변수가 참조하는 Heap영역내의 객체 이외의 다른 객체를 가리키도록 변경할 수 없다.
  + 메소드 : 오버라이드를 할 수 없다. (오버로드는 가능)
  + 클래스 : 해당 클래스를 상속받을 수 없다.

+ finally : catch/try 블럭에서 결과에 상관없이 수행되는 finally 블럭
+ finalize : 해당 객체가 GC의 대상이 될때 호출되는 메소드

</details>

-----------------------

<br>



<br>

-----------------------

### public static void main

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ public : JVM이 패키지나 클래스에 상관없이 어느곳에 존재하는 main함수를 호출 할수 있기 위함
+ static : JVM이 객체를 생성없이 main을 호출 할수 있기 위함
+ void : main함수가 JVM에 반환하는 것이 없음
+ main : 자바 프로그램 진입점

</details>

-----------------------

<br>



<br>

-----------------------

### Thread Safe

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 멀티 스레드 환경에서 여러 스레드로부터 동시에 접근이 이루어져도 각 스레드의 함수 수행결과가 올바르게 나오는 것.

+ Thread Safe하게 동작하는 방법
  + Re-entrancy
    + 어떤 함수가 스레드에 의해 호출되어 실행중일때, 다른 스레드가 그 함수를 호출하더라도 그 결과가 각각 올바르게 주어져야한다.

  + Thread-local storage
    + 공유자원 사용을 최대한 줄여 각 스레드에서만 접근 가능한 저장소를 사용하여 동시 접근을 막는다.

  + Mutual exclusion
    + 공유자원에 해당 자원의 접근을 뮤텍스, 세마포어 등으로 통제한다.

  + Atomic operations
    + 공유자원 접근시, 원자적으로 정의된 접근 방법또는 연산방법을 사용함으로써 상호배제를 구현할 수 있다.
      + 데이터 변경이 일어나고 있는 시점에는 접근이 불가능하다.
      
      + ```java
        int count = 0; //atomic operation
        count++; //non atomic operation
        	/*
        	1. count변수를 불러온다
        	2. count변수의 값을 증가시킨다.
        	3. count변수에 변경된 값을 저장한다.
        	count를 증가시키는 연산이 분리되어 적용되기 때문에 다른 스레드에 의해 값이 변경되었을때 올바른 값을 반환하지 못하는 문제가 발생할 수 있다.
        	*/
        ```



</details>

-----------------------

<br>



<br>

-----------------------

### 자료구조 특징 및 시간복잡도

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

+ List
  + ArrayList
    + 데이터를 순차적으로 저장하는 자료구조
    + 인덱스를 가지고 있어 검색에 효율적이다
    + 데이터 추가,삭제 시 성능 저하를 일으킴
    + thread-safe 보장 안함
    + 데이터 구조 : ArrayList
    + 시간복잡도
      + add : O(1)
        + 배열 복사 : O(n)
      + remove : O(n)
        + 배열 이동 : O(n)
      + get : O(1)
      + contains : O(n)
        + 내부적으로 indexOf를 통해서 배열 전체를 탐색하여 Object 여부를 확인한다.
  + LinkedList
    + 데이터의 이전 노드와 다음 노드의 상태만 알고 있는 자료구조
    + 데이터 추가,삭제시 효율적이다.
    + 인덱스 없이 순회하여 노드를 찾아야하기 때문에 느리다.
    + 데이터 구조 : LinkedList
    + 시간복잡도
      + add : O(1)
      + remove : O(1)
      + get : O(n)
      + contains : O(n)
        + 내부적으로 indexOf
+ Set
  + HashSet
    + 객체들을 순서를 보장하지 않고 저장하며 중복을 허용하지 않는다.
    + null을 허용한다, thread-safe 보장 안함
    + 저장을 목적으로하는 자료구조이기 때문에 get없다.
      + iterator로 순환 탐색
      + 내부적으로 HashMap으로 구현되어있고 key는 데이터의 해시, value는 더미값을 가지고 있어 map의 key를 get하는 것은 어렵다.
    + 데이터 구조 : Hash Map
    + 시간복잡도
      + add : O(1)
      + remove : O(1)
      + contains : O(1)
        + 해시 충돌로 최악의 경우 O(N)
  + LinkedHashSet
    + 객체들의 순서를 보장하며 중복을 허용하지 않는다.
    + null을 허용한다, thread-safe 보장 안함
    + 데이터 구조 : Hash Map + LinkedList
    + 시간복잡도
      + add : O(1)
      + remove : O(1)
      + contains : O(1)
      + get : O(1)
  + TreeSet
    + 객체 기준으로 정렬되며 범위 검색에 효율적이다.
      + 완전 이진 트리인 레드블랙 트리로 범위 탐색이 쉽도록 왼쪽노드는 작은값, 오른쪽노드는 큰값으로 정렬되어있기 때문
      + Subset()으로 범위 탐색 가능
    + 중복을 허용하지 않는다. null을 허용하지 않는다. thread-safe 보장 안함
    + 데이터 구조 : Red-black tree
    + 시간복잡도
      + add : O(logN)
      + remove : O(logN)
      + contains : O(logN)
+ Map
  + HashMap
    + key,value 형식으로 순서에 상관없이 저장되며 null을 허용하며 thread-safe 보장 안함
    + 시간복잡도
      + Put : O(1)
      + get : O(1)
      + containsKey : O(1)
  + LinkedHashMap
    + key,value 형식으로 순서를 보장하며 저장되며 null을 허용하고 thread-safe 보장 안함
    + 시간복잡도
      + Put : O(1)
      + get : O(1)
      + containsKey : O(1)
  + TreeMap
    + Key,value 형식으로 key으로 정렬되며 null을 허용하지 않고 thread-safe 보장 안함
    + hashMap은 탐색에 효율적이지만 TreeMap은 레드블랙트리로 이루어져있어 범위탐색과 정렬에 표과적이다.
      + Submap()을 통해 범위 탐색이 가능하다.
    + 시간복잡도
      + Put : O(logN)
      + get : O(logN)
      + containsKey : O(logN)
  + ConcurrentHashMap
    + Key,value 형식으로 쓰기 작업시에만 thread-safe보장, 읽기 작업에는 thread-safe 보장 안함
    + null 허용하지 않음
    + 시간복잡도
      + put : O(1)
        + synchronized를 적용하여 삽입 작업시 해당 **버킷**에 락을 걸어 동시성 문제를 해결
      + get : O(1)
        + 읽기 작업시에는 synchronized를 적용하지 않기때문에, 락이 걸리지 않고 최근 값을 읽어온다.
      + containsKey : O(1)
  + 기본적으로 Map의 구현체는 삽입과 탐색의 시간복잡도가 O(1)이게 된다. 하지만 해시 충돌로 인해 특정 해시에 데이터 쏠림이 발생하게 된다면 해당 해시에서 LinkedList로 선형탐색하여 데이터를 찾기때문에 O(n)이 발생할 수 있다.
+ Queue
  + PriorityQueue
    + 완전이진 트리인 Heap으로 구현된 자료구조로써 루트 노드에 가장 높은 우선순위의 데이터가 있다.
    + null을 허용하지 않고 Thread-safe 보장 안함
    + 데이터 구조
      + Heap
        + 완전이진트리 자료구조, 우선순위큐를 구현하기 위한 자료구조
        + 삽입 : 맨 끝노드에서 부터 비교하며 올라온다.
        + 삭제 : 루트노드를 삭제하고 맨 끝노드를 루트노드로 이동시키고 변경하며 내려온다.
    + 시간복잡도
      + offer : O(logN)
      + poll : O(logN)
      + remove : O(logN)
      + remove(Object) : O(n) // ?
      + contains() : O(n)
    
  + PriorityBlockingQueue
    + 일반적인 Queue구조로 우선순위가 높은 데이터 먼저 나가는 자료구조
    + null을 허용하지 않고 Thread-safe 보장
    + reentrantLcok을 사용해서 해당 자원에 하나의 스레드만 접근가능하도록 락을 걸어준다
      + reentrantLock은 뮤텍스처럼 시작과 끝에 lock과 unlock을 통해 하나의 스레드만 접근가능하도록 락을 걸어준다.


</details>

-----------------------

<br>



<br>

-----------------------

### Hash Table

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

+ Key,value 형태로 데이터를 저장하는 자료구조
+ key는 해시 함수를 통해 해시로 변경되어 value와 매칭되어 저장소에 저장된다.
  + key를 해시로 변경함으로써 고정된 길이를 가지게 되어 공간 효율성 추구
+ 고정크기의 해시 테이블이 가득차거나 체이닝의 길이가 길어지게 되면 검색 효율이 떨어지게 되므로, 버킷의 개수를 늘려주고 재해싱하는 리사이징을 해주어야한다.
+ 저장
  + key를 해시로 변경하여 value와 매칭하여 저장한다
  + 일반적으로 O(1)로 저장되지만 해시 충돌로 모든 value를 찾아봐야하는 경우 O(n)의 시간복잡도를 가진다.
+ 삭제
  + key와 매칭되는 value를 찾아서 삭제한다.
  + 일반적으로 O(1)로 삭제되지만 해시 충돌로 모든 value를 찾아봐야하는 경우 O(n)의 시간복잡도를 가진다.
+ 검색
  + key와 매칭되는 value를 찾는다
  + 일반적으로 O(1)로 검색되지만 해시 충돌로 모든 value를 찾아봐야하는 경우 O(n)의 시간복잡도를 가진다.
+ 해시 충돌
  + 서로 다른 값이 같은 해시 값을 가지게 되는 것.
  + 해결방법
    + Chaning
      + 해시 값이 충돌하게 되면 해당 값을 기존 값과 연결 리스트를 이용해 연결한다.
      + 8개 이상이 linkedlist 로 연결된다면 이진탐색트리로 저장하여 O(logN)으로 조회할수 있도록 한다. (**확실하지 않음**)
      + 장점
        + 한정된 저장소(Bucket)를 효율적으로 사용할 수 있다.
      + 단점
        + 특정 해시에 쏠림 현상이 발생하여 검색 효율을 낮출수 있다.
        + 외부 저장 공간을 사용한다.
    + Open Addressing
      + 해시 값이 충돌하게 되면 비어있는 해시를 찾아 데이터를 저장하는 방법
      + 주의사항
        + Open addressing은 탐색을 통해 빈 버킷을 찾아 값을 저장해주는 방식을 사용하는데, 특정 `중간 해시값이 삭제가되었을때 별도의 조치를 해주지 않는다면, 해시 충돌이 발생한적이 없다고 판단하게된다`.
          그렇기 때문에 `DEL`이라는 표시를 해주어 이전에 값이 존재했었고 해시충돌이 발생했을 가능성이 있다고 판단하여 다음 탐색을 이어나가 값을 찾을수 있도록 해주어야한다.
      + 장점
        + 추가적인 저장공간이 필요하지않다.
      + 단점
        + 해시함수의 성능에따라 해시테이블의 성능이 달라져, 해시함수의 의존도가 높다
      + 방법
        + 선형 탐색
          + 해시 충돌시 선형탐색으로 빈 버킷을 찾아 저장
          + 장점
            + 구조가 간단하다
          + 단점
            + 최악의 경우 해시 테이블 전체를 탐색하는 상황 발생
            + 클러스터 현상 발생
        + 2차 탐색
          + 원래 저장해야하는 위치로부터 특정 거리만큼 떨어진 영역을 검색하여 빈 영역에 저장
            + 탐색할 위치의 제곱값을 늘려준다 (1^2, 2^2, 3^2, 4^2 ...)
            + 장점
              + 선형탐색에서 1밀집 문제를 해결
            + 단점
              + 접근하는 위치가 항상 동일하기 때문에 연속 충돌발생 가능
              + 동일한 해시값에 대해 2차 클러스터 현상 발생
        + 2중 해시
          + 해시 충돌시 다른 해시 함수 적용
            + 첫번째 해시함수를 통해 해시 충돌이 발생했다면 다음 해시함수에서 탐색 이동폭을 구해주는 방법
          + 예를 들어 첫번째 해시함수는 k%3, 두번째 해시함수는 k%5일때, 입력값이 각각 3,6을 준다고 가정한다.
            첫번째 해시에서는 모두 0이 나와 해시 충돌이 발생한다. 그리고 두번째 해시함수에서는 각각 3,1이 되어 탐색 이동폭을 다르게 지정해 줄수있다.
            + 이때 해시함수의 식에서 나머지를 구하는 값은 k보다 작은 값을 사용하고, 소수인 값을 사용해야 클러스터 현상이 낮다는 통계가 있다
              + 클러스터 현상
                + 해시 공간에 특정 공간에만 데이터가 밀집되는 현상
                + 클러스터 현상이 적을수록 좋은 해시 테이블
        + Java8에서는 Separate Chaing사용
          + Open addressing에서는 해시 충돌시 빈 버킷공간을 찾기 위해 추가적인 비용이 발생하며, 삭제시에도 해시 충돌로 인한 값이 저장되었다면 표시를 해주어야하는 추가적인 비용이 발생한다.
          + 그렇기 때문에 별도의 저장공간을 사용하는 Separate Chainning방법을 채택한듯.
          + Java8에서는 기존 LinkedList로 충돌 값들을 저장하지만, 특정 값을 증가하게 되면 Tree(Red-black-Tree)로 변경하여 값을 저장.
            + LinkedList에서 저장 데이터가 8개이상이면 Tree로 변경
            + Tree에서 남은 개수가 6개가되면 LinkedList로 변경
            + Java7에서는 Entry를 사용했지만 Java8에서는 Node 클래스를 사용.
  + 데이터베이스의 인덱스에서 해시 테이블의 단점
    + 해시 테이블은 키값의 순서와 버킷의 순서와 연관성이 없기 때문에 데이터베이스에서 range query를 사용할때 해당 인덱스를 사용할 수 없다.


</details>

-----------------------

<br>



<br>

-----------------------

### 해시

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />





-----------------------

+ 해시는 데이터를 다루는 기법중 하나로서, 해시 함수를 이용해 동적 길이의 데이터를 고정 길이의 데이터(해시코드)로 변경하게된다.
  + 해시함수 : 길이가 다른 입력값을 입력하더라도 동일한 길이의 출력값을 생성하는 함수
  + 해시코드 : 해시함수를 통해 얻은 결과값

+ 해시코드는 해당 값의 고유값을 가지게 되므로 데이터 탐색시 빠른 성능을 제공한다. O(1)
+ 사용
  + 해시 테이블
    + 특정값의 고유 데이터로 반환해주는 것을 이용하여 해시의 key값으로 저장하면 빠른 탐색이 가능하다.
    + 해시 충돌 가능

  + 해시 알고리즘
    + SHA
      + 고정된 값 출력
      + 단방향 암호화이기 때문에 해시코드는 복호화 불가능 (보안성 우수)
      + 동일한 값에 대해서는 동일한 해시코드를 제공하지만, 조금이라도 다른값에 대해서는 완전히 다른 해시코드를 제공하기 때문에 데이터의 변조(데이터 무결성)을 확인하는데 사용된다.
      + 해시함수에 사용되는 알고리즘은 비교적 단순하기 때문에 자원낭비가 적게 들어 빠르게 해시값을 도출할 수 있다.

  + 데이터베이스 분산
    + 분산되어있는 데이터베이스에서 데이터를 고르게 분산하여 저장하기 적합하고 빠르게 접근할수있다.
    + 장점
      + 각 데이터베이스에 저장되는 데이터 양이 적어 관리가 쉽다

    + 단점
      + 어느 데이터베이스 서버에 어떤 데이터를 저장할지 고려할점이 많다
      + 특정 데이터를 저장하고있는 데이터베이스에 문제가 발생하면 해당 데이터에 접근할 수 없다
      + RDB인 경우 데이터의 연관관계가 많기 때문에 분리하기 어렵다.
        + NoSQL을 사용하면 스키마가 없기때문에 저장된 데이터를 JSON형식으로 저장할수있고 데이터의 관계에 상관없이 데이터를 저장하고, 불러올수있다.



</details>

-----------------------

<br>



<br>

-----------------------

### 정렬

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />



-----------------------

+ 선택 정렬

  + 현재 위치에 들어갈 값을 찾아 정렬

  + 최소 선택정렬시, 해당 위치부터 이후에 있는 모든 값을 비교하여 가장 작은 값과 해당 위치의 값과 변경하는 것이다.

  + ```java
    void selectSort(int[] arr){
      int index = 0;
      for(int i=0;i<arr.length;i++){
    		for(int j=i+1;j<arr.length;j++){
          if(arr[index] > arr[j]) index = j;
        }
        
        int temp = arr[index];
        arr[index] = arr[i];
        arr[i] = temp;
    	}
    }
    ```

  + 

  + 시간복잡도 : O(n^2)

    + 각 위치에서 뒤에있는 값과 모두 비교하기 때문에 n^2의 시간복잡도가 발생한다.

  + 공간복잡도 : O(n)

    + 하나의 배열에서 진행된다.

+ 삽입 정렬

  + 현재 위치에서 앞에 있는 값들과 비교하여 자신보다 큰 값과 작은값 사이에 삽입하여 정렬

  + ```java
    void insertSort(int[] arr){
      for(int i=1;i<arr.length;i++){
        int value = arr[i];
        int index = i-1;
        while(index>=0 && value < arr[index]){
          arr[index+1] = arr[index];
          index--;
        }
        arr[index+1] = value;
      }
    }
    ```

  + 시간복잡도 : O(n^2)

  + 공간복잡도 : O(n)

+ 버블 정렬

  + 두개의 요소를 비교하여 큰 값이 뒤로 가도록 변경해주면서 반복하는 정렬

  + 마지막 배열에 가장 큰값을 저장하므로 마지막 배열의 index를 하나씩 줄여가며 반복

  + ```java
    void bubbleSort(int[] arr){
      for(int i=0;i<arr.length;i++){
    			for(int j=0;j<arr.length-i-1;j++){
    				if(arr[j]>arr[j+1]){
    					int swap = arr[j];
    					arr[j] = arr[j+1];
    					arr[j+1] = swap;
    				}
    			}
    		}
    }
    ```

  + 시간복잡도 : O(n^2)

  + 공간복잡도 : O(n)

+ 합병 정렬

  + 더이상 나눌수 없는 크기 까지 나누고 (분할), 병합하는 과정에서 정렬하는 것 (병합)

  + ```java
    void mergeSort(int[] arr, int[] temp, int start, int end){
      if(start < end){
        int mid = (start+end)/2;
        mergeSort(arr, temp, start, mid);
        mergeSort(arr, temp, mid+1, end);
        merge(arr, temp, start, mid, end);
      }
    }
    
    void merge(int[] arr, int[] temp, int start, int mid, int end){
      //temp에 기존 값 저장
      for(int i=start;i<=end;i++){
        temp[i] = arr[i];
      }
      
      int part1 = start;	//왼쪽 파티션 첫번째 포인터
      int part2 = mid+1; 	//오른쪽 파티션 첫번쨰 포인터
      int index = start; 	//크기 비교된 값을 temp의 어디에 저장할것이지
      
      //왼쪽 파티션이나 오른쪽 파티션 중 모든 값을 정렬에 쓸때까지 반복
      while(part1 <= mid && part2 <= end){
        //왼쪽 파티션의 값이 더 작은경우 arr에 왼쪽 파티션값을 넣어준다.
        if(temp[part1] <= temp[part2]){
          arr[index] = temp[part1];
          part1++;
        }else{
          arr[index] = temp[part2];
          part2++;
        }
        index++;
        
        //왼쪽 파티션이 큰 경우 해당 값을 arr에 넣어주기 위한 작업
       	for(int i=0;i<=mid-part1;i++){
          arr[index+i] = temp[part1+i];
        }
        //오른쪽 파티션은 이미 큰값으로 정렬되어 있는 상태이기 때문에 arr을 넣어주는 작업이 필요없다.
      }
    }
    ```

  + 시간복잡도 : O(nlogn)

    + 배열을 나눌때 O(logn)이고 나누어진 배열에서 n개를 병합해야하기 때문에 nlogn

  + 공간복잡도 : 추가적인 저장공간피 필요함

+ 퀵 정렬

  + pivot을 배열의 중간값으로 선언하고 pivot을 중심으로 왼쪽에는 작은값, 오른쪽에는 큰값으로 이루어진 파티션을 만들어 각 파티션에서 pivot을 만들어 각 파티션으로 나누면서 정렬

  + ```java
    void quickSort(int[] arr, int start, int end){
      int part2 = partition(arr, start, end);
      
      //왼쪽 파티션이 2개이상 남아있다면 왼쪽파티션에 대해퀵정렬 계속
      if(start < part2-1){
        quickSort(arr, start, part2-1);
      }
      //오른쪽 파티션이 2개이상 남아있다면 오른쪽파티션에 대해 퀵정렬 계속
      if(part2 < end){
        quickSort(arr, part2, end);
      }
    }
    
    int partition(int[] arr, int start, int end){
       //피봇값 지정
       int pivot = arr[(start+end)/2];
      
      while(start<=end){
        //피봇값보다 큰 값을 찾을때까지 반복
        while(arr[start]<pivot) start++;
        //피봇값보다 작은 값을 찾을때까지 반복
        while(arr[end]>pivot) end--;
        //두 인덱스가 교차하지 않았다면 두 값 swap
        if(start<=end){
          int temp = arr[start];
          arr[start] = arr[end];
          arr[end] = temp;
          start++;
          end--;
        }
      }
      //두 값이 교차했을때 start가 pivot을 포함한 pivot보다 큰 값들이 정렬된 파티션
      //start는 해당 파티션의 시작 index이다.
      return start;
    }
    ```

  + 시간복잡도 : O(nlogn)

    + 보통 : nlogn, 최악 : n^2(pivot으로 선택되는게 최소또는 최대값인 경우)
    
  + while(start<=end) 인 이유
  
    + while(start<end)이게된다면, start=0, end=1인 경우 pivot은 index 0의 값을 가르키게 된다. 그렇게 되면 swap이 발생하지 않고 start = 0인 상태로 quickstart에 part2가 0으로 반환되게 되고 quckstart의 start=0, end=1로 무한 루프에 걸리게 된다.
    + pivot을 기준으로 pivot의 오른쪽 위치를 오른쪽 파티션으로 적용하고 그 왼쪽을 왼쪽 파티션으로 적용하기 위함.
  
  + if(start<=end)가 필요한 이유
  
    + start는 pivot보다 같거나 큰 값인 경우 멈추고 end는 pivot보다 같거나 작은 경우 멈추게된다. 이떄, if(start<=end)가 없다면 start>end가 엇갈리게 되는 경우가 발생할 수 있는데 이경우 start와 end가 swap될 경우 정렬이 무너지게 된다.
    + [1,1,8,2,3,4,7]의 배열인 경우, start = 2, end = 6, pivot = 1일 때 end는 1까지 감소되게 된다. 이때 if(start<=end)가 없기 때문에 swap이 발생하고 [1,8,1,2,3,4,7] 로 변경되어 정렬이 깨지게 된다.
  
+ 머지소트보다 퀵소트를 더 많이 사용하는 이유

  + 퀵소트는 최악의 경우 O(n^2), 보통 O(nlogn)이 걸린다. 머지소트는 평균 O(nlogn)이 걸린다.
  + 그렇기 떄문에 머지소트가 더 효율적이 아니냐할수 있겠지만, 퀵 소트의 최악경우는 pivot이 극단적인 값을 n번만큼 구해야하기 때문에 거의 그럴 경우가 없다.
  + 그리고 머지소트는 추가적인 메모리 공간이 필요하다. 하지만 퀵소트는 해당 배열에서 정렬이 수행되기 때문에 공간복잡도 면에서 효율적이다.
  + 머지소트는 끝에서 끝으로 분리된 원소들을 정렬하며 병합하는 과정을 거쳐 캐시에서 가지고 있지 않은 참조가 필요한 경우가 많아질 수 있다. 퀵 소트는 pivot을 중심으로 한정적인 공간을 정렬해 나가기 때문에 캐시에 있는 메모리를 자주 바꿀 필요가 없게 되어 캐시의 도움을 좀 더 받을 수 있다. 즉, 퀵 소트의 정렬이 캐시 지역성의 도움을 많이 받기 떄문에 머지소트보다 더 빠르다.


</details>

-----------------------

<br>



<br>

-----------------------

### Tree

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 비선형 자료구조로써 하나의 루트를 가지고 0개 이상의 자식 노드를 가지는 자료구조.
+ 이진트리
  + 자식 노드가 최대 2개인 트리구조
+ 완전 이진 트리
  + 이진트리에서 원소의 쏠림현상을 방지하기 위한 트리.
  + 왼쪽부터 오른쪽으로 채워야하며 마지막 level의 노드를 제외하고 나머지 level은 채워져 있어야한다.
  + 1개에서 2^h -1 개의 노드로 이루어져 있다.
+ 이진 탐색 트리
  + 효율적인 탐색을 하기 위한 트리.
  + 부모노드의 왼쪽자식노드는 부모노드보다 작은 노드, 오른쪽 자식노드는 부모노드보다 큰 노드
  + 데이터 쏠림현상으로 O(n)의 시간복잡도가 발생할 수 있다. 보통은 O(longN)
    + 삽입 : 삽입전에 탐색을 먼저 수행하게 된다. (중복값을 허용하지 않기 때문), 탐색에 실패했다면 그 자리가 삽입될 자리
    + 삭제 : 삭제할 노드와 가장 근사한 값을 가진 자식 노드가 대체된다.
+ 레드 블랙 트리
  + 이진 탐색트리에서 데이터 쏠림현상을 방지하기 위한 트리
  + 스스로 균형을 맞춘다.
  + 균형 이진 탐색트리이기 때문에 항상 O(logN)의 복잡도를 가진다.
  + 조건
    + 루트노드는 항상 검은색
    + 모든 leaf노드는 루트노드와 같은 검은색
    + 빨간 노드의 자식은 무조건 검은색, 검은색 노드는 검은색 자식을 가질 수 있다.
    + 모든 leaf노드에서 루트 노드까지 가는 경로의 검은색 노드 개수는 동일하다.
      + <img width="300" alt="image" src="https://user-images.githubusercontent.com/57162257/190675031-bd835690-a447-49a2-b357-945de97939fd.png">
  + 삽입
    + 삽입 할 때 노드는 항상 빨간색
    + 삽입시 부모노드가 빨간색이면 Double Red발생
      + 부모노드와 부모형제노드가 둘다 빨간색이면 ReColoring
      + 부모노드는 빨간색, 부모형제노드는 검은색이면 Restructing
    + ReColoring
      1. 부모노드와 부모형제노드를 빨간색에서 검은색으로 변경
      2. 조상 노드를 빨간색으로 변경
         - 조상 노드가 루트라면 검은색으로 변경
         - 그렇지 않고 빨간색으로 변경된 조상노드에 의해 DoubleRed발생시 ReColoring | Restructing 반복
    + Restructing
      1. 부모노드, 조상노드, 자식노드를 오름차순으로 정렬
      2. 가운데 값을 부모 노드로, 나머지 두 노드를 자식 노드로 변경
      3. 두 자식노드는 빨간색, 부모노드는 검은색으로 변경
  + B-Tree
    + https://rebro.kr/169
    + 2개 이상의 자식 노드를 가질 수 있는 밸런스 트리
    + 하나의 level에 여러 노드를 가질 수 있기 때문에 높이가 낮아서 다른 밸런스 트리보다 더 빠르게 탐색이 가능하다.
    + 시간복잡도
      + 탐색 : O(logN)
      + 삽입 : O(logN)
        1. 삽입할 데이터를 넣을 위치를 탐색
        2. 데이터 삽입
        3. 노드가 가득차게 된다면, 노드를 분할하고 가운데 값을 부모 노드로 이동시킨다.
        4. 부모노드도 가득차게된다면 반복
      + 삭제 : 
        + 삭제할 데이터가 리프 노드에 있는 경우
          + 삭제할 노드의 크기가 최소이고 형제 노드의 크기가 최소가 아닌 경우
            + 부모 노드를 삭제 노드에 삽입, 형제 노드의 최대또는 최소의 값을 부모 노드에 삽입
          + 삭제할 노드의 크기와 형제 노드의 크기가 모두 최소인 경우
            + 부모 노드값을 형제노드에 삽입하여 부모 노드의 크기를 줄인다.
        + 삭제할 데이터가 리프 노드를 제외한 노드에 있는 경우
          + 자식 노드의 크기가 아닌 값이 있는 경우
            + 최소가 아닌 자식 노드에서 왼쪽 자식 노드라면 최대값, 오른쪽 자식 노드라면 최소값을 swap하고 swap되어 리프노드에 있는 부모값을 삭제하고 삭제과정 수행
          + 삭제할 노드와 자식 노드의 크기가 모두 최소인 경우
            - 삭제할 노드를 삭제하고 자식 노드를 병합하고 형제 노드에 부모노드 값을 불러와 병합한 자식 노드를 연결해준다.



</details>

-----------------------

<br>





### Heap

-----------------------

### 

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 힙속성을 만족하는 완전 이진 트리 구조
  + 힙 속성 : 부모와 자식간의 크기 조건
  + Max heap이라면 부모노드가 자식노드보다 커야한다.

+ 종류
  + max heap : 루트노드가 가장 큰 값을 가져야하고, 부모노드는 자식노드보다 커야한다.
  + min heap : 루트노드가 가장 작은값을 가져야하고, 부모노드는 자식보다 작아야한다.

+ Binary Heap
  + 이진 트리 구조인 힙 (자식 노드가 최대 2개)
  + 완전 이진 트리 구조이기 때문에 공간낭비가 적다.

+ 삽입 : 마지막 노드에 원소가 저장되고 부모 노드와 비교하여 크기 조건이 일치하지 않으면 swap, 크기 조건이 맞을때까지 반복
+ 삭제 : 루트노드가 삭제되고 마지막 위치의 노드가 대체되어 크기 조건을 비교하며 swap
+ 정렬 : 원소를 삽입시 logN의 시간복잡도로 루트에 값이 정렬된다. 이를 N번 수행하면 NlogN


</details>

-----------------------





<br>

-----------------------

### Tree

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />




-----------------------

+ 


</details>

-----------------------

<br>

