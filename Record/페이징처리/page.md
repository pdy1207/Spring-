### 우선 페이징 처리를 하려면

 - 한 페이지에 게시물 몇개 보여줄지? <br>
    ex) 네이버웹툰 기준 1page 10개 게시물 보여줌 <br><br>
 - 한 블록에 몇개 페이지 보여줄지? <br>
    ex) 네이버 웹툰 기준 1블록에 10page

![1](https://user-images.githubusercontent.com/110442250/193737129-243c27e7-b03e-48d9-a9f3-5d547b5ace64.jpg)
 - 윗 사진처럼 쿼리스트링으로 페이징 처리를 구현한다.
 - 쿼리스트링 ??  @RequestParam : URL을 보게되면... & ? 등등 값을 입력받을때 보통 파라미터값에 등록을 하게된다. //쿼리스트링!!

        우선 임포트를 먼저 하자!! 
        //page
        implementation group: 'com.github.pagehelper', name: 'pagehelper-spring-boot-starter', version: '1.4.2'

![3](https://user-images.githubusercontent.com/110442250/193737166-a578eed1-3de0-4a59-a638-3efcb928a321.jpg)
![4](https://user-images.githubusercontent.com/110442250/193737168-a1ad3197-1897-4d23-ae28-9a3f2097333f.jpg)
![5](https://user-images.githubusercontent.com/110442250/193737170-2cc7b3ad-556e-470f-b2bf-f361749e77bd.jpg)
