# Java



<br>

-----------------------
### Java란

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------
+ Java
    + 자바는 객체지향 언어로써 객체지향의 특징을 사용하여 프로그램을 만드는 컴파일러 언어이자 인터프리터 언어이다.
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

+ 인터프리터 언어
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
  + 객체가 상속을 통해 기능을 확장하거나 변경하여 다른 형태로 재구성하는 것.
  + 오버라이딩(Overriding) : 자식 클래스가 부모 클래스의 메소드를 입맛대로 변경해서 구현하는 것
  + 오버로딩(Overloading). : 부모 클래스의 같은 이름의 메소드를 사용해도 매개변수나 데이터 타입을 다른 형태로 재구성 하는 것.

+ 캡슐화(Encapsulation)
  + 객체가 하나의 목적을 위해 필드와 메소드를 하나의 캡슐로 묶은 것.
  + 정보은닉을 목적으로 접근제어자를 통해 캡슐화된 객체의 정보를 제어한다.
    + private : 해당 클래스에서만 접근 가능
    + default : 해당 패키지 내에서만 접근 가능
    + protected : 해당 패키지 내의 클래스와 해당 클래스를 상속받은 클래스에서만 접근 가능
    + public : 모든 곳에서 접근 가능

+ 추상화(Abstraction)
  + 객체의 공통적인 속성과 기능을 추출하여 정의하는 것.
  + 인터페이스 : 공통으로 구현해야하는 것을 정의.
  + 추상 클래스 : 공통으로 구현해야하는 것을 정의하고 공통으로 사용하는 필드와 메소드를 선언.



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

+ 인터페이스는 구현을 약속하여 구현 객체의 같은 동작을 보장하는것이 목적이다.
+ 추상 클래스는 상속받아서 기능을 이용하고 확장하는것이 목적이다.
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
  + 추상화 된것은 구체적인 것에 의존하면 안된다. 구체적인 것이 추상화된 것에 의존해야 한다.
  + 변화하기 쉬운것보다 변화하기 어려운것에 의존해야한다.
  + ex) 자동차는 변하기 쉬운 구체적인 타이어에 의존하면 안된다.
    + 타이어 종류에는 스노우타이어, 일반 타이어, 광폭타이어 등이 있어서 타이어가 변경될 때마다 자동차에 영향을 준다.
    + 자동차는 구체적인 타이어가 아닌 추상화된 타이어에 의존하여 타이어가 변경되어도 자동차가 영향을 받지 않아야 한다.
    + <img src="/Users/flab1/Library/Application Support/typora-user-images/image-20220728232039710.png" width="50%">


</details>

-----------------------

<br>



<br>

-----------------------

### 객체지향 프로그래밍 vs 절차지향 프로그래밍

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 절차지향 프로그래밍 
  + 실행하고자 하는 절차를 정하고 순차적으로 프로그래밍 하는 방법
  + 빠르게 구현할 수 있지만 절차가 정해져있기 때문에 유지보수가 어렵다.

+ 객체지향 프로그래밍
  + 구현하고자 하는 객체들의 상호작용을 프로그래밍 하는 방법
  + 상속, 다형성, 캡슐화, 추상화를 통해 결합도를 낮추고 응집도를 높일 수 있으며, 코드 재사용률을 높일 수 있다.



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
    + 각 Thread는 메소드를 수행하고 PC Register는 해당 메소드의 몇번째 줄을 실행해야하는지 나타낸다.
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
+ GC 알고리즘
  + Reference Count
    + 객체를 참조하는 개수를 나타내는 reference count가 0이라면 GC의 대상이되는 알고리즘
    + 두 객체가 서로를 참조한다면 reference count가 영구적으로 1이되기 때문에 GC의 대상이 되지않는 문제가 발생할 수 있다.

  + Mark and Sweep
    + root에서 부터 해당 객체에 접근가능한 객체는 `Mark`, 접근이 불가능한 객체는 GC의 대상이되어 삭제(`Sweep`)

+ GC 동작과정
  1. Young Generation의 Eden영역이 포화상태가 된다.
  2. Stop the World 발생 후 Mark and Sweep 실행(Minor GC)
  3. 살아남은 객체는 survival 0영역에 저장된다.
  4. survival 1영역이 포화되면 Minor GC 실행
  5. 살아남은 횟수 age가 일정 횟수가 된다면 Old Generation 영역에 저장된다.
  6. Old Generation이 포화상태가 되면 Major GC발생.
+ GC 종류
  + Serial GC : 하나의 스레드로 GC 수행
  + Parallel GC : java 8의 default GC, 여러 스레드로 GC 수행
  + G1 GC : java 9의 default GC, Heap을 여러 영역(Young Generation, Old Generation)으로 나누어 GC 수행
    + 통상적으로 객체의 생명주기는 짧기 때문에 대부분 Young Generation영역에 존재한다. 그렇기 때문에 GC 탐색 범위를 최소화 하기 위함이다.

+ 장단점
  + 장점 : 메모리 누수 방지, 해제된 메모리 접근 방지
  + 단점 : GC가 언제발생할지 모름

+ 주의 사항
  + Major GC는 Minor GC보다 실행시간이 훨씬 오래걸리며 Stop the World로 인해 실시간 프로그램에서 크리티컬한 이슈가 발생할 수 있다.
  + GC 모니터링을 통해 코드를 리펙토링하거나 GC튜닝을 하여 GC를 처리하도록 한다.



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

+ 

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

+ 


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

+ 


</details>

-----------------------

<br>



<br>

-----------------------

### 참조 타입

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 


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

+ 


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

+ 

</details>

-----------------------

<br>



<br>

### Call By Value vs Call By Reference

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 

<img width="60%" alt="image" src="https://user-images.githubusercontent.com/57162257/181691033-9553a6ef-09d2-4844-bfd4-ab9e16695d8e.png">


</details>

-----------------------

<br>



<br>

-----------------------

### String

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 

<img width="50%" alt="image" src="https://user-images.githubusercontent.com/57162257/181692343-8d8792b1-09dd-40d1-ba6f-7460e64c84bc.png">

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

+ 


</details>

-----------------------

<br>



<br>

-----------------------

### Java Collections

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


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

+ 


</details>

-----------------------

<br>





<br>

-----------------------

### Java란

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

+ 



</details>

-----------------------

<br>