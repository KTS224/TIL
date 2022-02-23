# TIL (Today I Learned)🔥
2022-02-11

# 데이터 타입
모든 데이터타입 이름은 첫 글자가 대문자로 시작하는 대문자 카멜케이스를 사용한다

## 불리언(Bool)
```swift
var someBool: Bool = true
// true 또는 false 값만 갖을 수 있다.
```
## 정수(Int)
```swift
var someInt: Int = 1000
// 정수값만 가능

var someUInt: UInt = 100
// 0과 양의 정수값만 가능   -> -부호 불가

someInt = someUInt       // (x) 타입이 달라서 오류 발생 
someInt = Int(someUInt)  // (o) 
```
## 실수(Float,Double)
```swift
var someFloat: Float = 3.123
//32비트의 부동소수 표현

var someDouble: Double = 123133.2123
//64비트의 부동소수 표현
```
## 문자(Character)
```swift
var someCharacter: Character = "A"
someCharacter = "♡"
someCharacter = "ㅁ"
// 한글자만 가능 
```

## 문자열(String)
```swift
var someString: String = "hello"
//문자열 
someString.append(" world!")
someString = someString + " world!!" 
//문자열 이어붙이기

print(someString) //hello world! world!!

print(someString.isEmpty) //false
//빈 문자열인지 참 거짓 판별가능

print(someString.count) //20
//문자의 수 세기


print(someString.hasPrefix("hell")) // true
// 문자열이 () 로 시작 하는지 Bool 값으로 확인  

print(someString.hasSuffix("!!"))  //true
// 문자열이 () 로 끝나는지 Bool 값으로 확인

print(someString.uppercased())  
// 대문자 변환. HELLO WORLD! WORLD!!

print(someString.lowercased()) 
// 소문자 변환. hello world! world!!