# Ruby 정복하기(2)
> `Note` | 본 포스트는 공식 Ruby on Rails Guides 및 opentutorials의 Ruby Coin 강좌를 정리한 것임을 알림

## 0. Ruby On Rails란
### Rails란 무엇인가
레일즈는 루비 언어로 작성된 웹 어플리케이션 프레임워크이다.  가이드에 따르면 레일즈는 "최고"의 방법을 가정하고, 그러한 방법을 격려하도록 설계되어 있다고 한다. “레일즈의 방법(The Rails Way)” 배우면, 아마도 굉장한 생산성 향상을 경험할 것이며 만약 다른 언어의 개발 습관들을 레일즈 개발시 고수하고 있다면, 아마 덜 행복한 경험을 .

레일즈의 철학은 몇 가지 원칙을 포함합니다.

-   DRY  – “Don’t Repeat Yourself (반복하지 말 것)” – 이 원칙은 ‘같은 코드가 존재한다면 그것은 나쁜 것’을 의미합니다.
-   설정 보다 관습(Convention Over Configuration) – 이 원칙은 여러분이 원하는 기능들에 대해서 일정한 가정을 바탕으로 해결책을 제공하여 작은 단위의 끝없는 설정 파일을 줄여줍니다.
-   REST  는 웹 어플리케이션의 최고의 패턴이다.- 리소스와 표준  HTTP  요청(HTTP  verb)에 적합한 웹 어플리케이션 개발은 가장 빠른 방법입니다.


## 1. 기본구조 파악하기
### 서버가 하는 일
Rails 서버는 MVC 패턴으로 이루어져 있기 때문에 Model, View, Controller가 서로 상호작용하여 정보를 가공하게 된다.

-   Model : 어플리케이션의 데이터와 정보를 다루는 규칙을 담당한다
-   View : 데이터 표현에 대한 부분을 담당한다
-   Controller: Model과 View를 이어주며, 데이터 가공을 수행한다.
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDk2MDkwODg0XX0=
-->