# Spring DB연결 하기 전에 오타에 주의하자 

### spring DB연결을 하려면 우선적으로 필요한 소스들

**1. gradle에 데이터베이스 라이브러리 추가 (무조권첫번째)**
 
          gradle , maven ...등등
          maven mysql 검색 
          URL : https://mvnrepository.com/artifact/mysql/mysql-connector-java
          
          
      JDBC문제점 
      sql요청을 할 때 마다 jdbc에 재로그인.
      ORM(Object Relation Mapping)
      JAVA ORM 종류 Mybatis, JPA(어려움...시간날때 검색)
          
 - 이제 사진을 참고해보자

![1](https://user-images.githubusercontent.com/110442250/190061792-fe438333-c7f4-4a2a-9585-81687d1df0b9.jpg)

![2](https://user-images.githubusercontent.com/110442250/190061799-cb0f336a-e16a-4405-96b4-7545537f0b47.jpg)

![11](https://user-images.githubusercontent.com/110442250/190064759-09c339b7-8992-44ad-b4f3-acddebd74e2d.jpg)

![3](https://user-images.githubusercontent.com/110442250/190061805-8ba97119-00f4-4b91-a9c5-7db42f30493a.jpg)

![4](https://user-images.githubusercontent.com/110442250/190061810-813c89c1-4e47-452f-9aa2-6f2dd645b832.jpg)

## 2. 속성파일(application.properties)에 DB 아이디,비밀번호 작성 

          properties 확장명을 yaml(야믈)로 수정
          차이점 : 야믈이 더 알아보기가 쉬운거같음 Maybe... 개인차
          복사본 (사진참고)
          DB 접속 정보 입력
          
## 3. Spring 과 Mybatis(ORM) 연결

      resources경로에 sqlmap 폴더 생성 (new -> Package)
      sqlmap에 xml파일 생성 (이름은 sqlmapper_하고싶으이름.xml)
      속성파일(yaml)에 sqlmapper_*.xml 경로 작성
      
      

# 단, DB접속 정보는 다릅니다. 파일 등 오타 조심하세요. 사진 참고

![8](https://user-images.githubusercontent.com/110442250/190064082-89807cd2-e083-4315-9143-38839ee6a31b.jpg)

![9](https://user-images.githubusercontent.com/110442250/190064112-ee8dbfb9-aa83-4288-aaf0-6c284be32f39.jpg)

![10](https://user-images.githubusercontent.com/110442250/190064121-682cabb3-172e-455c-90db-3fb3e3c60d26.jpg)

![5](https://user-images.githubusercontent.com/110442250/190063253-2a1e0bb7-7529-469f-8f05-adb671e8bee4.jpg)

![7](https://user-images.githubusercontent.com/110442250/190063517-eddacf96-ecb0-4c18-8816-cd0f65aa1256.jpg)

![6](https://user-images.githubusercontent.com/110442250/190063263-96c45338-b2cf-44c7-98ad-6b644a24e996.jpg)

