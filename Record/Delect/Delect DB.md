## 지금 하고 있는 데이터베이스가 어떤거에 관하여 중요하다.

 - 학원 기준 / 관계형 데이터 베이스 이다 (Mysql, Oracle, MariaDB...) </br>
   관계형이란? join 삭제 가 엄격하니 부모와 자식을 잘 보자.

 - 참조키를 사용하고 있는 테이블이 자식 테이블(emp)이 된다. </br>
   참조키를 제공하는 테이블은 부모 테이블(dept)이 된다.

 - 자식테이블에서 데이터 삭제는 자유롭지만,</br>
   부모테이블은 자식테이블과 관계가 있기 때문에 삭제가 어렵다.</br>
   이미지를 먼저 봐보자.
   
   ![1](https://user-images.githubusercontent.com/110442250/194444483-dd1cea42-383f-4d88-b081-19e3582f457e.jpg)
   
 -  부모테이블 delete쿼리 부모테이블 : 참조키를 제공하니 부모테이블임.</br>

        DELETE 
        FROM dept 
        WHERE DEPTNO = 30; //실행안됨.


 - 자식테이블 delete쿼리 자식테이블 : 참조키를 사용하니 자식테이블

        DELETE 
        FROM emp 
        WHERE deptno = 30 실행됨.


 - 그렇다면.. 부모테이블에 데이터를 삭제해보자 </br>
   함수가 어떤건가?
   CASCADE 설정을 해야한다.

### 정리를 하자면

 - 자식테이블의 삭제는 자유롭다 </br>

 - 부모테이블의 삭제는 자유롭지않다 </br>
   그럼 어떻게?

 - CASCADE 를 줘야한다 그래야 부모테이블 삭제가 자유롭다.</br>
   그러나, 데이터는 곧 자산이므로 SET NULL로한다.</br>

          -- ON DELETE는 관계형 데이터베이스만 존재(Oracle, mysql, MairaDB...)

          -- ON DELETE CASCADE : 부모테이틀에 데이터를 지우면,
          -- 참조하고 있는 자식테이블 데이터도 모두 지워진다.

          -- ON DELETE SET NULL : 부모테이블에 데이터를 지우면, 
          -- 참조하고 있는 자식테이블에 컬럼이 NULL 로 변경된다.

          -- ON DELETE RESTRICT(default) : 부모 테이블 데이터를 지울 때,
          -- 자식 테이블에서 데이터를 참조 하고 있다면 삭제, 변경 불가능


          -- ON DELETE NO ACTION : 부모 테이블에서 데이터를 지우면,
          -- 자식 테이블에 아무런 영향을 받지 않는다.

          -- ON DELETE SET DEFAULT  : 부모 테이블에 데이터를 지울 때, 
          -- 참조하고 있는 자식테이블 컬럼이 DEFAULT 값으로 변경된다.


## 아! 맞다!! FK안에 못 넣었다.... 지웠다가 넣는이유는 ON DELETE SET NULL ...을 넣기위함.
     
      ALTER TABLE emp DROP FOREIGN KEY FK_DEPTNO; //기존의 pk와 관계도를 없앤다.


      //관계도를 재설정한다.
      ALTER TABLE emp ADD CONSTRAINT FK_DEPTNO FOREIGN KEY (DEPTNO) 
      REFERENCES DEPT(DEPTNO) ON DELETE SET NULL;
      
      
 - 쉽게 말하면 이말인데 여기서 정리를 해보자면.....
 - ALTER TABLE "자식 테이블" DROP FOREIGN KEY FK_"연결된 FK";
 - ALTER TABLE "자식 테이블" ADD CONSTRAINT FK_"연결된 FK" FOREIGN KEY ("연결된 FK")
 - REFERENCES DEPT("연결된 FK") ON DELETE SET NULL; // ON DELETE CASCADE , ON DELETE NO ACTION , ON DELETE SET DEFAULT.....
