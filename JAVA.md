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
  + 장점
    + 번역된 코드를 실행만 시키면 되기 때문에 실행 속도가 빠르다.
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
  + 하나의 객체가 여러 가지 타입을 가질 수 있는 것
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
  + 인터페이스 : 공통으로 구현해야하는 것(강제)을 정의하여 구현체에게 기능 구현을 강제하고 동일한 동작을 목적으로 한다.
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

+ 인터페이스는 구현을 강제하여 구현 객체의 같은 동작을 보장하는것이 목적이다.
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
    + <img width="426" alt="image" src="https://user-images.githubusercontent.com/57162257/185022337-b9fbcde6-c136-4dd5-bd01-2ee639b099a5.png">


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
  + 문제를 해결하기 위해 순차적으로 프로그래밍 하는 방법
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
+ GC 종류
  + Serial GC : 하나의 스레드로 GC 수행
  + Parallel GC : java 8의 default GC, 여러 스레드로 GC 수행
  + G1 GC : java 9의 default GC, Heap을 여러 영역으로 나누어 GC 수행
    - <img width="304" alt="image" src="https://user-images.githubusercontent.com/57162257/187113600-2594d63f-9214-4cf4-835e-814379d7f7fb.png">
    - young, old generation 영역을 명확하게 구분하는 전통적 heap과 다르게 eden, survivor, old, unused등의 작은 region으로 나누어져있다.
    - 장점 
      - young, old영역을 전체 탐색하는 것이 아닌, 특정 영역에 있는 Garbage를 제거함으로써 처리 속도가 빠르고 빠르게 빈 공간을 확보하기 때문에 GC의 빈도도 낮아진다.
    - 단점
      - Major, minor GC가 발생해도 공간이 부족한 경우 싱글 스레드로 Full GC가 발생하여 GC 처리 속도가 느리다.
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
  4. survival 0영역이 포화되면 Minor GC 실행
  5. 살아남은 횟수 age가 일정 횟수가 된다면 Old Generation 영역에 저장된다.
  6. Old Generation이 포화상태가 되면 Major GC발생.
+ 장단점
  + 장점 : 메모리 누수 방지, 해제된 메모리 접근 방지
  + 단점 : GC가 언제발생할지 모름
+ 주의 사항
  + Major GC(Full GC)는 Minor GC보다 실행시간이 훨씬 오래걸리며 GC실행시 발생하는 Stop the World로 인해 실시간 프로그램에서 크리티컬한 이슈가 발생할 수 있다.
  + old영역으로 넘어가는 객체 수를 줄이기 위해 String보다는 StringBuilder나 StringBuffer를 사용하고 로그 수를 줄인다. 그리고 Old영역의 크기를 조절해서 Full GC의 빈도를 줄이고 GC수행 시간을 적게 하도록 잘 조절한다.


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
  + 1개의 문자만 저장하는 원시타입

+ String
  + 문자열 주소를 저장하는 참조타입

+ char는 원시타입이기 때문에 동일성 비교(==)가 가능하지만 String은 참조타입이기 때문에 동일성 비교시 참조 주소를 비교하기 때문에 같은 value를 비교하기 위해서는 동등성 비교(equals())를 해야한다.

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
  + ""선언은 Heap의 String Pool에 저장이되며 같은 value일 때 동일성 비교가 가능하다.
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

### Java Collections

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />


-----------------------

<img width="70%" alt="image" src="https://user-images.githubusercontent.com/57162257/181880446-bea276d3-7c23-472a-9fc7-3d9946d27b25.png">

여러 원소를 담을 수 있는 자료구조로 Set과 List는 Collection을 상속하고 Map은 Collections를 직접 상속받고 있다.

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
    - 모든 작업(쓰기, 읽기) 동기화
  - ConcurrentHashMap
    - HashMap과 동일한 동작을 한다.
    - key와 value의 null을 비허용한다.
    - 쓰기작업만 동기화

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
  + Stream : stream()을 호출하는 시점부터 요소를 계산한ㄷ.

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
  + repeat(n) : 문자열을 n번 반복하여 반환

+ Collection의 toArray()메소드를 오버로딩하는 메소드가 추가되어 원하는 타입의 배열을 선택하여 반환.
  + <img width="514" alt="image" src="https://user-images.githubusercontent.com/57162257/181903621-6b0527b5-cddf-4fd7-b6e0-46202a0bd9ac.png">

+ 람다 표현식에서 지역변수에 var 사용이 가능해져 컴파일 시 타입을 추론하게 하고 타입에 사용할수 있는 어노테이션을 사용할 수 있다..
  + <img width="561" alt="image" src="https://user-images.githubusercontent.com/57162257/181903638-846ceb6c-6dc8-4294-bcc9-519a7b696492.png">

+ javac로 컴파일하지 않고 java파일을 수행할 수 있다.

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

    + synchronized block시 인자에 this로 걸어주게 되면 this를 인자로 가진 synchronized block은 모두 lock이 걸리게 된다. 만약 synchronized block별로 lock을 걸어줄 메소드를 지정해주려면 Object1, Object2 등의 별도로 선언한 객체로 동기화 처리를 할 synchronized block의 인자로 정의하게 되면 object1으로 정의한 메소드끼리 동기화가되고 object2로 정의한 메소드끼리 동기화가 된다.

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
+ 멀티스레딩을 수행할 클래스는 Runnable 인터페이스를 상속받아 run()을 구현하여 Thread 생성자의 인수로 넘긴다.


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
