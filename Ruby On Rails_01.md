# Ruby On Rails 정복하기(1)
> `Note!`  
> 본 포스트는 공식 Ruby on Rails Guides 및 opentutorials의 Ruby Coin 강좌를 정리한 것임을 알림

## 1. Rails란 무엇인가
레일즈는 루비 언어로 작성된 웹 어플리케이션 프레임워크이다.  가이드에 따르면 레일즈는 "최고"의 방법을 가정하고, 그러한 방법을 격려하도록 설계되어 있다고 한다. 

“레일즈의 방법(The Rails Way)” 배우면, 아마도 굉장한 생산성 향상을 경험할 것이라고 한다. 내가 고수해오던 기존 Node.js 기반의 개발과 어떠한 차이점이 있는지 차차 알아가보려 한다.

레일즈의 철학은 몇 가지 원칙을 포함한다.

-   `DRY`  “Don’t Repeat Yourself (반복하지 말 것)” => ‘같은 코드가 존재한다면 그것은 나쁜 것’
-   `설정 보다 관습(Convention Over Configuration)` 원하는 기능들에 대해서 일정한 가정을 바탕으로 해결책을 제공 => 작은 단위의 끝없는 설정 파일을 줄여줌
-   `REST  는 웹 어플리케이션의 최고의 패턴이다` 리소스와 표준  HTTP  요청(HTTP  verb)에 적합한 웹 어플리케이션 개발은 가장 빠른 방법이다.


### 1. MVC  아키텍쳐
레일즈의 중심에는  MVC  라고 불리는 모델, 뷰, 컨트롤러 아키텍쳐가 있다. MVC의 장점은 다음과 같다.

-   유저 인터페이스와 비지니스 로직 분리
-   DRY  유지 편이성
-   더 쉬운 유지보스를 위한 코드 관리 편이성

##### 1.1 모델(Models)
모델은 어플리케이션의 정보(data)와 데이터를 다루는 규칙들을 의미한다. 레일즈의 경우에, 모델은 주로 데이터베이스 테이블과 상호 작용하는 규칙들을 관리한다. 대부분의 경우에 데이터베이스의 하나의 테이블은 어플리케이션의 하나의 모델과 대응한다. 대부분의 비지니스 로직은 모델에 집중된다.

##### 1.2 뷰(Views)
뷰는 어플리케이션의 유저 인터페이스를 의미한다. 레일즈에서 뷰는 주로 데이터 표현에 관련 된 루비 코드가 삽입되어 있는  HTML  파일이다. 뷰는 데이터를 웹 브라우저나 다른 기기에게 데이터를 제공하는 일을 담당한다.

나의 경우에는 View단을 Vue.js 프레임워크를 사용할 예정이다.

##### 1.3 컨트롤러(Controllers)
컨트롤러는 모델과 뷰를 "연결"하는 역할을 한다. 레일즈에서 컨트롤러는 웹브라우저의 요청 받아서, 모델을 통해서 데이터를 조회하여, 출력을 위해 뷰에게 데이터를 넘겨준다.

### 2.  REST

REST는 Representational State Transfer 를 의미하고 RESTful 아키택쳐의 근간이 된다. 레일즈의 존재하는  REST  두가지 중요한 원리는 다음과 같다.

-   자원 표현을 위해 자원 식별자 사용 (가령  URL)
-   시스템 컴포넌트 간에 자원 상태 교환

예제로, 레일즈 어플리케이션에서 요청은 다음과 같다.

DELETE  /photos/17

이 것은 photo 리소스 ID 17번 참조하고, 원하는 액션은 삭제라고 이해할 수 있다. REST는 웹 어플리케이션의 아키텍쳐상 자연스로운 형태이고, 레일즈는 어플리케이션을 RESTful 복잡성과 브라우저의 변덕스러운 요청에서 보호한다.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5Nzk5OTYwMzksLTE3NjQ0Njk0NTIsLT
gyMzIzOTIyOF19
-->