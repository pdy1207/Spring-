-- 로그 테이블 생성하기 </br>
-- AUTO_INCREMENT 자동으로 값이 1씩 증가

        CREATE TABLE IF NOT EXISTS emp_logs(
          log_id bigint(20) AUTO_INCREMENT PRIMARY KEY COMMENT '로그 번호',
          ip varchar(50) COMMENT '사용자 아이피',
          url varchar(100) COMMENT '접속 경로',
          http_method varchar(10) comment 'http method',
          create_at datetime comment '접속 시간'

        )

-- insert 컬럼이름 명시하는 문법</br>
-- ex) insert into emp (empno) values(2000)</br>
-- 컬럼이름을 명시하는 insert는 다른 컬럼들 생략가능.</br>
-- 단, 다른 컬럼들이 not null이라면 그 컬럼은 넣어야 함 .</br>

-- insert 컬럼이름 생략 문법</br>
-- insert into emp values(2000) </br>
-- 해당 테이블 데이터 모두 입력해야함.</br>

============================================================================================
- 요구사항

어떤 요청이 오든 method, url, ip를 알고싶음.

HttpServletRequest를 메소드 마다 만드는건 비효율적이라고 생각함.

Spring 인터셉터  (중간에 가로챈다,preHandle)

Spring에서 모든 사용자 요청을 인터셉터 한다.

ex) 사원 조회 요청 -> 인터셉터!(preHandle) -> Controller -> postHandle

![2](https://user-images.githubusercontent.com/110442250/196090085-48183990-2e20-452c-99ba-f1feba01413b.jpg)
