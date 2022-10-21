
# Spring 으로 데이터베이스 연동 방법

    1-1 구글에 maven mysql 검색
    1-2 mvnrepsitory.com 접속
    1-3 mysql gradle용 복사
    1-4 build.gradle에 붙여넣기
    1-5 mvnres''사이트에서 mybatis 검색
    1-6 MyBatis Spring Boot Starter 클릭 ( 4번째)
    1-7 mybtis gradle용 복사 -> build.gradle에 붙여넣기
    1-8 build.gradle 새로고침
    (build.gradle 우클릭 -> gradle -> refresh gradle (end)


    2. 속성파일에 DB 아이디, 비밀번호 작성
    2-1 application.properties 확장명을 yaml(야믈)으로 수정
    2-2 DB 접속 정보 입력

    3. Spring과 Mybatis(ORM) 연결
    3-1 resources경로에 sqlmap 폴더 생성 (new -> package)
    3-2 sqlmap에 xml 파일 생성 (이름은 sqlmapper_하고싶은이름.xml)
    3-3 속성파일(yaml)에 sqlmapper_*.xml 경로 작성

    4. 결과 확인하기
      4-1. xml에 쿼리 작성
