# Let's Build with Ruby On Rails - (1)
이 시리즈는 Ruby on Rails에 관한 것입니다. 우리는 app들을 만들고 프레임워크에 대한 다음의 토픽들을 다루며 지식을 확장시킬 것입니다. 
- MVC patterns, CRUD 
- databases, migrations, generators 
- stylesheets, javascript
- ruby, rails

> `Note`
> Web Crunch - [Let's Build: With Ruby On Rails] 강좌를 정리한 내용임을 알림
> [https://web-crunch.com/series/](https://web-crunch.com/series/)


## 1. Introduction
 블로그, 뉴스피드, 작은 유저기반 앱 등을 만들어 볼 것입니다.
 
## 2. Installation
Ruby On Rails 설치

## 3. A Blog with Comments
Ruby On Rails를 이용해 댓글 작성이 가능한 **블로그**를 만들어 보는 것은 이 프레임워크를 배워감에 있어 기본적인 경험이 될 것입니다.

또한 Ruby와 Rails를 함께 사용하면 **CRUD 접근 방식 기반**의 상당히 간단한 **MVC 패턴**을 구현할 수 있기 때문에 **동적 데이터를 다루기 용이**합니다.

### 블로그로 시작하는 이유
basic한 블로그 제작을 통해 Ruby On Rails의 동작 원리를 쉽게 배울 수 있습니다. 

각각의 포스트들은 `생성(created)`, `조회(read)`, `수정(edited)`, `삭제(deleted)`가 가능할 것입니다. 또한 각 게시물에는 댓글을 작성할 수 있도록 할 것입니다. 댓글들은 `생성`과 `삭제`가 가능합니다.

이 프로젝트를 위해 우리는 몇가지의 `gems`를 사용할 것인데 이는 application 만드는 것에 도움을 줍니다.

### 프로젝트에 사용되는 Gems
- Better Errors - 에러가 발생했을 때 보기 쉽게 해줌
- Bulma - CSS Framework
- Guard -  useful for live reloading scss, js, css and erb files

### 프로젝트 생성
`$ rails new demo_blog` : demo_blog 프로젝트 생성
`$ cd demo_blog` : 만든 프로젝트 폴더로 이동
`$ rails s` : 서버 3000 on, 잘 돌아가는지 확인

### gem 설치
demo_blog/Gemfile 에 다음을 추가
- better_errors
- bulma-rails
- simple_form
- guard
```ruby
# Make errors better looking
gem 'better_errors', '~>2.4'
# Bulma CSS
gem 'bulma-rails', '~> 0.6.1'
# Simple Form
gem 'simple_form', '~> 3.5'

group :development do
					...
	# Guard is a command line tool to easily handle events on file system modifications.
	gem 'guard', '~> 2.1.4', '>=2.14.1'
	# reload the browser after changes to assets/helpers/tests
	gem 'guard-livereload', '~> 2.5', '>= 2.5.2', require: false
					...
end
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgzODU1ODM2NCwxODIwNzk4NDcsLTE1Nj
M1ODQ3MTUsMTI2NjU3MDg3NSwtODkzNzMxMTksLTMxNzg1ODUx
MSw5MDEyNzcxNTZdfQ==
-->