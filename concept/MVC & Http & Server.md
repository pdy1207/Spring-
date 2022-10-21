### MVC
    
    M(Model == Mapper&Service)  V(View) C(Controller) 는 
    규모가 큰 프로젝트에서 업무분담을 하기위해 사용하는 적절한 디자인 패턴 (== 코드 아키텍쳐) 중 하나 

    장점 : 유지보수가 쉬움 , 직관적임, 인력 채용 쉬움
    단점 : 규모가 작다면 시간낭비, 가독성 떨어짐

    Point : MVC는 spring 뿐만 아니라 여러 프레임워크에서 사용하는 디자인 패턴이다.
    MVC는 spring 기술이 절대아님!!!!
    
    
### Mybatis

	xml 파일에 sql문을 작성하면
	mybatis라는 orm 소프트웨어가
	db에 접속해서 sql실행 후 결과를 
	자바소스로 매핑(연결)시켜줌  
    
    
### 패키지

    Spring에서 패키지를 만들 때는
    최소 3개 부터 만들어야함! 
    controller - url 정의 HTTP method 정의
    service - 로직 구현 + serviceImple (service 인터페이스)
    mapper - SQL 매핑 (==연결)
    VO(Value Object) : getter, setter만 존재하는 클래스(*Java에서만 사용하는 개념 x )
    
### !HTTP method!

    GET : SELECT
    POST : INSERT
    PATCH : UPDATE
    DELETE : DELETE 

### http 오류

    HTTP method! (시간날때 구글링 해보기)
    http 메소드가 다르면 url경로 중복 가능
   
    404 : 페이지를 찾을 수 없음 90% 오타
    ex) 경로 (URL)을 잘못 씀
          잘못된 경로
    ex) Controller에서 URL 정의했는데
	    /emp/job
	프론트에서 ajax로 요청할 때 url에 
	    /emp/jop???? 오타!!!!  
        
    405 : http 메소드 (get, post, delete, patch) 매칭 실패
    ex ) Controller에 get이라고 만들었는데, 프론트에서 post라고 함.
    오류 뜨면 type 먼저!!
    
    500 : Java에서 에러(SQL문법 오타, 자바에서 문법 오류..) / 개발자 실수 (프로그래밍 오류)
    
    401 : 권한 없음
    (권한 없어서 해당 URL 접속 불가능)
    
    200 : !!!요청 성공!!!
 
    
### 서버 (Server)

    서비스를 제공해주는 컴퓨터 => 서버
    서비스 종류 : 게임, 데이터베이스...

    내 PC에 A프로그램을 설치함 
    A를 설치하면 내 PC에 접속할 수 있음.

    localhost:8080/emp
    localhost: 서버 주소
    8080 : 서버 방 주소(포트 번호)

    http://192.168.0.20:8080/emp
    DNS(도메인 네임 서버)
    https://www.naver.com
    https의 디폴트 포트번호는 80이다.
    https http에 보안을 강화함 (유료)




