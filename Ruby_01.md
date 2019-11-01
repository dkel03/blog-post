# Ruby 정복하기 (1)
## 1. 해쉬와 반복자
### 해쉬

> #### 루비의 Dictionary 자료형

해쉬(hash)는 배열의 일종으로, 인덱스를 숫자 뿐만 아니라 문자와 같은 모든 종류의 객체를 사용할 수 있는 데이터 타입이다. 해쉬는 연관배열(associate array)라고도 부른다.

해쉬는 key와 value의 쌍으로 구성된다. 사전에서 구름이라는 단어(key)를 통해 구름의 뜻(value)을 찾듯이 해쉬도 key값을 통해 value를 찾을 수 있다. 때문에 다른 언어에서는 해쉬를 사전(dictionary)라고도 한다.
해쉬는 다음과 같이 생성한다.

```ruby
grades = {"Soohorang" => 9, "Bandabi" => 7}
```
위에서 Soohorang은 key가 되고 9는 value가 된다. 마찬가지로 Bandabi는 key가 되고 7은 value가 된다. 해쉬는 다음과 같이 다른 방법으로도 생성할 수 있다.

```ruby
grades = Hash.new
grades["Soohorang"] = 9
grades["Bandabi"] = 7
```
해쉬에서는 다음과 같이 key값을 통해 value의 값을 가져올 수 있다

## 2. 메소드와 코드 블록

## 3. 모듈
### 모듈
모듈(module) 이란 메소드나 클래스, 상수들을 묶는 방법으로서, 특정한 기능을 수행하는 부품이다.

모듈은 관련있는 상수와 메소드를 하나로 묶어놓을 때 사용하거나 Ruby에서 제공하는 믹스인(mix) 기능을 위해서 사용한다.

다음과 같은 cafe.rb 모듈이 있다고 가정하자.

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
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE4ODgzNTY5NywxNDM5NjM4OTQ4LDkyNz
IyNDZdfQ==
-->