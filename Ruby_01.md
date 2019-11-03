# Ruby 정복하기 (1)
> **Note** 본 포스트는 Osam.kr의 Ruby 강좌를 정리한 것임을 알림
## 1. 해쉬와 반복자
### 해쉬

> #### 루비의 Dictionary 자료형

해쉬(hash)는 배열의 일종으로, 인덱스를 숫자 뿐만 아니라 문자와 같은 모든 종류의 객체를 사용할 수 있는 데이터 타입이다. 해쉬는 연관배열(associate array)라고도 부른다.

해쉬는 key와 value의 쌍으로 구성된다. 사전에서 구름이라는 단어(key)를 통해 구름의 뜻(value)을 찾듯이 해쉬도 key값을 통해 value를 찾을 수 있다. 때문에 다른 언어에서는 해쉬를 사전(dictionary)라고도 한다.
해쉬는 다음과 같이 생성한다.

```ruby
grades = {"Soohorang" => 9, "Bandabi" => 7}
```
위에서 **Soohorang**은 **key**가 되고 **9**는 **value**가 된다. 마찬가지로 **Bandabi**는 **key**가 되고 **7**은 **value**가 된다. 해쉬는 다음과 같이 다른 방법으로도 생성할 수 있다.

```ruby
grades = Hash.new
grades["Soohorang"] = 9
grades["Bandabi"] = 7
```
해쉬에서는 다음과 같이 **key**값을 통해 **value**의 값을 가져올 수 있다

## 2. 메소드와 코드 블록

## 3. 모듈
### 모듈
**모듈(module)** 이란 메소드나 클래스, 상수들을 묶는 방법으로서, 특정한 기능을 수행하는 부품이다.

모듈은 관련있는 상수와 메소드를 하나로 묶어놓을 때 사용하거나 Ruby에서 제공하는 믹스인(mix) 기능을 위해서 사용한다.

다음과 같은 **cafe.rb** 모듈이 있다고 가정하자.

> 모듈은 같은 파일에서 생성할 수도 있고, 다른 파일에서  생성할 수도 있다. 다른파일에서 모듈을 생성하고 사용하는 방법에 대해 알아보자
```ruby
#data/cafe.rb
module Cafe 
	module_function() 
	def show_menu(beverage) 
		puts "Menu" beverage.each {|name, price| puts "#{name}\t#{price}"} 
	end
	def show_price(beverage, select) 
		beverage.each do |name, price| 
			if select == name 
				return "#{price}원 입니다" 
			end 
		end 
		return "그런 음료는 판매하지 않습니다" 
	end 
end
```
모듈은 `module`이라는 키워드로 시작하여 모듈 이름을 적고 `end`로 마친다. 모듈의 이름은 반드시 대문자로 시작해야 한다. 위의 코드에서는 **Cafe**라는 이름을 가진 모듈을 생성하였다.

- `module_function()` 은 다른 파일에 모듈을 생성하였을 때, 모듈안에 있는 여러 메소드들을 접근 가능하도록 만들어주는 내장 메소드이다.
- `show_menu()` 메소드는 **beverage**라는 입력값(해쉬)를 받으면 그 내용을 출력해주는 메소드이다.
- `show_price()` 메소드는 **beverage**(해쉬)와 select라는 입력값을 받는다. select와 **beverage**라는 해쉬 값 내의 **key**를 비교하여 일치하는 값이 있으면 **value**값을 포함한 문자열을 리턴하고 그렇지 않으면 다른 문자열을 리턴한다.

다음은 **main.rb**라는 파일에서 **cafe.rb** 파일의 **Cafe 모듈**을 활용한 예제이다.
```ruby
#main.rb 
require './data/cafe' 

beverage = {'coke' => 3000, 'juice' => 4000, 'tea' => 6000, 'coffee' => 5000} 

Cafe.show_menu(beverage) select = 
gets.chomp() puts 
Cafe.show_price(beverage, select)
```
- require는 모듈이 작성된 파일을 불러와 사용하기 위해서 작성한다. 우리가 사용할 cafe 모듈은 cafe.rb파일에 있기 때문에 require 뒤에 cafe.rb 파일의 디렉토리를 작성한다.

## 4. 클래스와 객체 이론
Ruby는 객체 지향 언어이며 모든 것이 객체로서 표현된다. 문자열, 숫자, true와 false, 심지어 클래스 자체도 모두 객체로 표현된다.

### Ruby에서 클래스 정의하기
객체 지향 프로그램은 클래스(class)와 객체(object)라는 개념을 포함하고 있다.

클래스란 객체의 형태를 지정할 때 사용되며 데이터


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI3MzIwMDE1NiwtMTQ4NjI0MDQ0NCwxND
M5NjM4OTQ4LDkyNzIyNDZdfQ==
-->