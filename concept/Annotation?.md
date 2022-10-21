# Spring Annotation(@) 정리

      Annotation 이란?
      사전적으로는 "주석"이라는 의미를 가지고 있으며, 
      자바 코드에 @를 이용해 주석처럼 달아 특수한 의미를 부여해준다.
      프로그램 코드의 일부가 아닌 프로그램에 관한 데이터를 제공하고, 
      코드에 정보를 추가하는 정형화된 방법이다.
      어노테이션을 사용하면 코드가 깔끔해지고 재사용이 가능하다.

# Spring 
 - `@CrossOrigin` : 누구나 자원(소스)를 요청할 수 있게 권한 해제
 - `@Autowired` : new 자동생성 (Spring 이 클래스를 관리해준다.)    
 - 프레임워크 (Spring boot) 가 클래스를 관리해주는 기술을 Dependency Injection(DI)
 - `Service` : 비즈니스 계층 (고객 요구사항) 여기서 구현하겠다

# 오버로딩 & 오버라이딩 정리
 - `오버로딩(Overloading)`
   - 동일한 이름의 메소드 작성가능
   - 단, 파라미터 개수, 파라미터 데이터 타입은 달라야 성립
 
 - `오버라이딩(Overriding)`
   - 인터페이스 혹은 클래스를 상속받아서 메소드를 재정의하는 것

# ㄱㄱ 

 - `@SpringBootApplication`</br>
Srping Boot를 자동으로 실행시켜주는 어노테이션

 - `@Autowired`</br>
이 Annotation을 사용할 시, 스프링이 자동적으로 값을 할당한다.

 -`@Controller`</br>
      Spring MVC의 Controller로 사용되는 클래스 선언을 단순화 시켜주는 어노테이션</br>
       -- 여기서 MVC 는? M(Model == Mapper&Service)  V(View) C(Controller) 

 - `@Service`</br>
비지니스 로직이 들어가는 Service로 사용되는 클래스임을 명시하는 어노테이션

 - `@RequestMapping`</br>
클라이언트에게 요청받는 주소를 클래스와 연결시켜주는 어노테이션 (클래스 연결 중간점) / 디폴트 GET 방식</br>
클래스와 메소드단 두 곳에서 모두 사용 가능

 - `@CrossOrigin`</br>
다른 출처의 자원을 공유할 수 있도록 설정하는 권한, 외부 접속도 허용해준다.
 
 - `@GetMapping` : 조회 
 - `@DeleteMapping` 말그대로 삭제 어노테이션
 - `@PatchMapping` : 정보 수정할때  
 - `@PostMapping` : 둘다( & Patch) 보통 적으로 RequestBody로 받아옴. (숨겨서 보내주기때문 무엇을? 우리가 입력된 값을)
                  </br>보통 등록할때 사용
헷갈릴만 해서 쉽게 설명하면.. 파라미터 값이 많다 `RequestBody` || 적다 `@PathVariable`  
 - `@RequestParam` : URL을 보게되면... & ? 등등 값을 입력받을때 보통 파라미터값에 등록을 하게된다. //쿼리스트링!!

 URL EX) 이러한것들이 이제 쿼리스트링으로 해야한다.
![1](https://user-images.githubusercontent.com/110442250/193729831-73c2db54-1815-4c1b-9edd-1596e5afccd7.jpg)

    사이트 중 ? : 쿼리 스트링 
    사이트 내에서 값을 입력받겠다 라는 뜻
    @PathVariable처럼 
    url에 값을 넘겨주는 방법 중 하나. 

    url에 값을 넘겨주는 방법
    1. path ex) /emp/{empno} 값을 하나 넘겨줄때 즉 길어질땐 비추
    2. ? / emp?empno=3 (쿼리스트링) 길어질땐 이 방법 선호

    url(controller)

    값을 하나만 넘길 때 path 사용 
    여러 값을 넘길 때 queryString사용


 ### 다 POST로 받아도 된다. 그렇지만........이런식으로는 하지마세요.

