# TIL (Today I Learned)🔥
2022-02-09

## 함수 (Func)

```swift
func plusTwo(x: Int) -> Int {
    return x + 2
}
```
인수(함수에 전달받은값,argument)가 들어오고, 

반환값(return value)이 나간다

 x -> x + 2

- 매개변수(parameter) : 인수가 전달될 자리


## print함수
```swift
print(1,2,3 , separator: "!")
//separator: "m"    각 인자 사이의 띄어쓰기를 "m"로 바꿔준다

---> 1!2!3


print(1,2,3,terminator: " ")
print(4,5)
//terminator: "m"   줄바꿈을 하지않고 대신 "m" 출력

---> 1 2 3 4 5


"   " 안에 인자를 넣으려면 
print("\(name)은 이름")  // \()로 묶어준다
```
### 변수
-  var {이름} = {값}

### 상수 
- let {이름} = {값}
  
  - 상수는 값을 할당하면 변경불가



## 네이밍

- 숫자로 시작 불가
- 띄어쓰기 불가
- 특수문자는 $ 또는  _ 허용되지만 $ 첫글자로 사용불가
- 변수나 함수의 이름 첫글자는 소문자로 시작하자
- 변수의 이름은 명사 . 함수의 임름은 동사로 시작하자
