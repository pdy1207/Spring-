# CRUD
	
      개념부터 알아보자
      
      API 서버를 만들 때 URL 작성 법 
      아래 규칙을 준수하는 API RestFul API 서버라고 함.
      (시간날 때 RestFul 검색)
      
      resultType은 SQL결과 return type이다.

	 우선적으로 resources 안에있는 

	 쿼리에 컬럼이름과 VO 클래스에 변수이름은 동일해야 한다.

	 Id에 Interface에서 정의한 메소드 이름을 넣는다.
	 
      1. 대문자 보다는 소문자로 작성!
        ex ) /wfootball/record/index ( o )
             /wfootball/RECORD/index ( x )

      2. 동사 보다는 명사를 사용한다. (*특히 중요)
        ex ) /emp ( o )
        ex ) /emp/update ( x )

      3. 마지막에는 / 를 입력하지 않는다.
        ex ) /emp/sal ( o )
        ex ) /emp/sal/ ( x )

            contentType : 서버에 요청 데이터 타입
            dataType : 서버에 응답받결과 데이터타입
            data : 서버에 보낼 데이터!
            success : 요청 성공!!!
            html : 500이면 자바 확인하기
            앞글자가 4다 자바스크립트
        
     
## select : GET / insert : POST / update : PATCH / delete : DELETE

 ### 우선 spring 문법을 봐보자 
 ## 1. insert : POST

![1](https://user-images.githubusercontent.com/110442250/191159679-e5605f52-0a05-4fe3-9800-0aa0a4bfacc1.png)
![2](https://user-images.githubusercontent.com/110442250/191159682-37f38bc4-c9eb-4d59-9e15-25cb053338a9.png)
![3](https://user-images.githubusercontent.com/110442250/191159684-0918288b-6dbc-44c1-bce9-2dab29ddb9fd.png)

## 2. delete : DELETE

![4](https://user-images.githubusercontent.com/110442250/191159686-8586c0b4-9879-4419-b227-b54e248b60a7.png)
![5](https://user-images.githubusercontent.com/110442250/191159687-d6af5cbf-cfc6-4972-b699-c78e5264fccc.png)
![6](https://user-images.githubusercontent.com/110442250/191159688-e3eb60ce-e600-42a9-b3f7-960f1502b3b8.png)

## 3. select : GET 사원번호로 사원조회 

![1](https://user-images.githubusercontent.com/110442250/191427234-e5ede8b4-e315-4cfb-9288-5b476342fd9a.png)
![2](https://user-images.githubusercontent.com/110442250/191427239-8d4f5aea-a87c-4491-9710-9f6d6bc8afb8.png)
![3](https://user-images.githubusercontent.com/110442250/191427242-7e0296ad-e730-4702-a22a-9953adfd0be4.png)
![4](https://user-images.githubusercontent.com/110442250/191427243-afb752b3-697a-462c-aa1c-b5ac7471710b.png)

## 4. update : PATCH 사원 업데이트 

![5](https://user-images.githubusercontent.com/110442250/191427406-1c4cc49e-b8df-48b3-8280-203e02dba31d.png)
![6](https://user-images.githubusercontent.com/110442250/191427410-74f23f50-013e-4840-b9b6-8650931efe1b.png)
![7](https://user-images.githubusercontent.com/110442250/191427412-5f65a03a-1bdc-4ce9-94c7-22f4c7cdebc8.png)
![8](https://user-images.githubusercontent.com/110442250/191427414-57941641-cdb8-487d-89cd-5333f8317fa2.png)
![9](https://user-images.githubusercontent.com/110442250/191427416-acd37114-9023-4e03-bf05-a65f6d1af543.png)

## 5. 최종적인 전체 조회

![10](https://user-images.githubusercontent.com/110442250/191427715-d48f8dc0-4ea5-4f90-8171-78075a132c00.png)
![11](https://user-images.githubusercontent.com/110442250/191427723-444911e2-0ac4-490b-b6db-b582d600428c.png)
![12](https://user-images.githubusercontent.com/110442250/191427725-5c430174-0047-4067-b874-39d247de2264.png)
![13](https://user-images.githubusercontent.com/110442250/191427728-3c483230-ab02-4049-bb87-09fbd2f047ac.png)

