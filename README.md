# Start to Ruby on rails :)

## Ruby란?

- 스크립트 언어
- 객체 지향 프로그래밍 언어

## Ruby의 특징

1. 자유로운 형식

   - 들여쓰기가 크게 중요하지 않은 언어
   - 일반적으로 두 자 들여쓰기를 하는게 좋음

2. 대소문자의 구분

3. 주석

   - 한 줄 단위의 주석

   ``` ruby
   # 한 줄 주석이에오
   ```

   - 주석 블록

   ```ruby
   =begin
   여러 줄의 주석을 작성할 때는
   이렇게 써주세오
   =end
   ```

4. 문장 구분 기호

   - 줄바꿈 만으로도 구분
   - 한 줄에서 여러 구문을 사용한다면 세미콜론(;)으로 구분

   ```ruby
   boram = 'student'
   puts boram
   age = 23; pust age;
   ```

5. 키워드

   - 약 42개의 키워드
   - 변수, 클래스의 이름으로 사용 불가
   -  `false`는 0 이나 `null` 등으로 표현
   - `false`와 `nil`을 제외한 모든 값들은 `true`

   

| `BEGIN`  | `do`     | `next`     | `then`     |
| -------- | -------- | ---------- | ---------- |
| `END`    | `else`   | `nil`      | `true`     |
| `alias`  | `elsif`  | `not`      | `undef`    |
| `and`    | `end`    | `or`       | `unless`   |
| `begin`  | `ensure` | `redo`     | `until`    |
| `break`  | `false`  | `rescue`   | `when`     |
| `case`   | `for`    | `retry`    | `while`    |
| `class`  | `if`     | `return`   | `yield`    |
| `def`    | `in`     | `self`     | `__FILE__` |
| `module` | `super`  | `__LINE__` | `defined?` |

## 출력하기

- `puts` : 한 줄 단위로 출력
- `print` : 계속 이어서 출력

```ruby
print "Hello World!"
puts 'Hello World'
```

- `upcase()` : 문자열을 대문자로 출력
- `downcase()` : 문자열을 소문자로 출력
- `length()` : 문자열의 길이를 출력

```ruby
name = 'Boram'
puts name.upcase()		# BORAM
pusts name.downcase()	# boram
puts name.length()		# 5
```

## 변수

- 변수(variable) : 숫자나 문자열과 같은 정보를 저장할 수 있는 컨테이너
- 할당(assignment) : 변수에 정보를 담는 것, 일반적으로 오른쪽의 항의 값이 왼쪽 항으로 할당

``` ruby
name = 'boram'
puts '나는 ' + name + '이다!'	# 나는 boram이다!
```

## 입력하기

- `gets.chomp()` 

```ruby
puts '성별을 입력해주세요. '
gender = gets.chomp()
puts '성별은' +  gener + '입니다. '
```

## 산술연산자

- 산술연산자( Arithmetic Operator) : 수학적 계산을 수행할 때 사용하는 연산자

| 연산자 | 설명                            | 예시 ( a, b = 10, 3) |
| ------ | ------------------------------- | -------------------- |
| +      | 더하기 연산자                   | a + b     # 13       |
| -      | 빼기 연산자                     | a - b     # 7        |
| *      | 곱하기 연산자                   | a * b     # 30       |
| /      | 나눗셈의 몫을 구하는 연산자     | a / b     # 3        |
| %      | 나눗셈의 나머지를 구하는 연산자 | a % b     # 1        |
| **     | 거듭제곱 연산자                 | a **b     # 1000     |

## boolean 자료형

- `true` : 결과가 참
- `false` : 결과가 거짓

```ruby
puts true
puts false
```

## 비교 연산자

- 비교 연산자(Comparison Operator) : 두 개의 피연산자의 관계를 비교하기 위해 사용하는 연산자
- 비교한 결과가 boolean 자료형인 true나 false로 반환

```ruby
a, b = 3, 5
puts (a == b)	# false
puts (a < b)	# true
puts (a > b)	# false
puts (a <= b)	# true
puts (a >= b)	# false
puts (a != b)	# true
```

## 대입 연산자

- 대입 연산자(Assingnment Operator) : 계산과 대입이 결합되어 있는 연산자를 의미

```ruby
a, b = 7, 4
a += b; puts a;	# a = 11

c, d = 11, 8
c -= d; puts c;	# c = 3

e, f = 9, 5
e *= f; puts e;	# e = 45

g, h = 13, 5
g /= h; puts g;	# g = 2

i, j = 13, 5
i %= j; puts i;	# j = 3

k, l = 3, 4
k **= l; puts k; # k = 81
```

## 논리 연산자

- 논리 연산자( Logical Operator) : AND, OR, NOT을 표현할 수 있는 연산자

- 논리 연산자의 결과는 boolean 자료형인 true(참)와  false(거짓)으로 표현

  | 논리연산자 | 기호 |
  | ---------- | ---- |
  | AND        | &&   |
  | OR         | \|\| |
  | NOT        | !    |

## 조건문 if - elsif - else - end

```ruby
if 조건
  코드.......
elsif
  조건 외에 여러가지 조건을 고려하고 싶을 때 사용
else
    코드......
end	
```

## 반복문 while - do - end

```ruby
while 조건 do
  코드...
end
```

```ruby
# while 문을 이용하여 10부터 1까지 역순으로 출력하기
i = 10
while i >= 1 do
    puts i
    i = i - 1
end
```

## 반복문 for - end

```ruby
for 변수 in 표현 [do]
  코드.....
end
```

## 배열

- 배열(array) : 연관된 데이터를 모아서 관리하기 위해 사용하는 데이터 타입
- 원소(element) : 대괄호 안에 담긴 각각의 데이터들

```ruby
fruit = ['apple', 'orange', 'mango', 'plum', 'berry']
mix = ['ruby', 'coding', 2018, true]
```

- 인덱스(index) : 원소를 식별하기 위해 사용, 첫 번째 원소는 인덱스가 0부터 시작

| 인덱스 | 0     | 1      | 2     | 3    | 4     |
| ------ | ----- | ------ | ----- | ---- | ----- |
| 값     | apple | orange | mango | plum | berry |

- new() 메소드를 이용해서 배열을 생성할 수도 있음

```ruby
names = Array.new
```

- 배열의 크기를 미리 지정하는 방법

```
names = Array.new(20)
puts names.size
puts names.length
```

- 배열의 값을 미리 지정하는 방법

```ruby
names = Array.new(5, 'ruby')
puts names	# ['ruby', 'ruby', 'ruby', 'ruby', 'ruby']
```

## 해쉬

- 해쉬(hash) : 배열의 일종으로, 인덱스를 숫자 뿐만 아니라 문자와 같은 모든 종류의 객체를 사용할 수 있는 데이터 타입
- 연관배열(associate array), 사전(dictionary) 라고도 부름
- key와 value의 쌍으로 구성

```ruby
grades = {"Soohorang" => 9, "Bandabi" => 7}
```

- new 메소드를 이용해서 해쉬를 생성할 수 있음

```
grades = Hash.new
grades["Soohorang"] = 9
grades["Bandabi"] = 7
```

## 반복자

- 반복자(iterator) : 배열에서 사용할 수 있는 메소드의 일종

#### each

- 파이프(||) 사이에 선언한 변수에 배열의 값을 하나씩 담아와서 실행

```ruby
arr = [1, 2, 3, 4, 5]
arr.each {|a| puts a}
arr.each do |a|
	puts a
end
=begin
출력결과
1
2
3
4
5
=end
```

#### collect

- 파이프(||) 사이에 선언한 변수에 배열의 값 각각을 사용하여 새로운 배열을 생성

```ruby
a = [1, 2, 3, 4, 5]
b = a.collect {|x| x*10}
puts b
=begin
출력결과
10
20
30
40
50
=end
```

tmi -> Ruby에서는 배열과 해쉬를 collections 이라는 용어로 부름

```ruby
grades = {"Soohorang" => 9, "Bandabi" => 7}
grades.each{|k, v| puts "Key: #{k}, Value: #{v}"}
=begin
출력 결과
Key: Soohorang, Value: 9
Key: Bandabi, Value: 7
=end
```

## 메소드

- 메소드(method) : 함수, 항상 소문자로 시작

```ruby
def hello()					# 함수 선언
    puts "Hello, Ruby!"		# 코드 작성
end							# 함수 종료
hello()						# 함수 호출
```

- 메소드는 리턴값(return)을 가질 수 있음

```ruby
def hello()
    str = "Ruby"
    return str
end
puts(hello())
```

- 메소드는 입력값(parameter) 또한 가질 수 있음
- 입력값은 메소드의 이름 옆에 있는 ()에서 지정

```ruby 
def hello(num)
    return 'Ruby'*num
end
puts (hello(3))
```

- 메소드는 여러개의 입력값을 가질 수 있음

```ruby
def hello(str, num)
    return str*num
end
puts (hello('boram', 3))
```

## 코드 블록

- 블록(block) : 필요한 기능을 묶어 사용할 수 있는 기능
- 블록은 코드의 덩어리로 구성
  - 코드의 덩어리들은 항상 중괄호({})로 묶임
  - do와 end 사이에도 작성할 수 있음

#### 숫자. times() 

- 숫자만큼 같은 동작을 반복하는 메소드

#### 숫자1.upto(숫자2)

- 숫자1부터 숫자2까지 같은 동작을 반복하는 메소드

```ruby
5.times() {|i| puts i}
3.upto(5) {|i| puts i}
=begin
출력 결과
0	# 5.times() {|i| puts i} 의 결과
1
2
3
4
3	# 3.upto(5) {|i| puts i} 의 결과
4
5
=end
```

- 블록은 항상 블록의 이름과 같은 이름을 가진 메소드에 의해서 호출
- 메소드 내에서 블록을 호출할 때 yield라는 키워드를 사용

```ruby
# 메소드
def my_method
    puts 'start'
    yield
    puts 'end'
end
# 블록
my_method do
    puts "yield"
end
```

- 메소드가 입력값을 받을 수 있는 것처럼 yield를 사용하여 블록이 입력값을 받기

```ruby 
# 메소드
def my_method
    yield("goorm", 6)
end
# 블록
my_method do |name, age|
    puts "#{name} is #{age} years old"
end
```

- yield를 사용하여 블록의 리턴값을 가져올 수도 있음

```ruby
# 메소드
def my_method
    value = yield
    puts "value from block : #{value}"
end
# 블록
my_method do
    10
end
```

```ruby
# 구구단을 출력하는 블록
# 메소드
def googoo
	yield(5)
end
# 블록
googoo do |dan|
	for i in 1..9
		puts "#{dan} x #{i} = #{dan*i}"
	end
end
```

