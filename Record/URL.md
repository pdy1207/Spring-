- 요구사항

어떤 요청이 오든 method, url, ip를 알고싶음.

HttpServletRequest를 메소드 마다 만드는건 비효율적이라고 생각함.

Spring 인터셉터  (중간에 가로챈다,preHandle)

Spring에서 모든 사용자 요청을 인터셉터 한다.

ex) 사원 조회 요청 -> 인터셉터!(preHandle) -> Controller -> postHandle

![2](https://user-images.githubusercontent.com/110442250/196090085-48183990-2e20-452c-99ba-f1feba01413b.jpg)
