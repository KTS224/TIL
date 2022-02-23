# TIL (Today I Learned)🔥

2022-02-22

<br>

```swift
var number = 100

func add(to number: Int) -> Int {
    number += 1
    return number
}
```

![https://s3.ap-northeast-2.amazonaws.com/media.yagom-academy.kr/resources/usr/61ee3b7c2947bf40f08f32e4/20220223/6216150d536b5e1551d11006.png](https://s3.ap-northeast-2.amazonaws.com/media.yagom-academy.kr/resources/usr/61ee3b7c2947bf40f08f32e4/20220223/6216150d536b5e1551d11006.png)



1을 더하는 함수를 만들었는데 

이처럼 오류가 나왔다.

<br>

```swift
func addOne(to number: Int) -> Int {
    var functionNumber = number
    functionNumber += 1
    return functionNumber
}

print(addOne(to: number))  // 101
print(number)  // 100
```

이렇게 함수안에 변수를 선언하면 답은 나오지만 

다시 `number` 를 출력했을 때 값은 변하지 않았다.

그렇게 구글링해본결과

<br>

# inout

```swift
func addTwo(to number: inout Int) -> Int {
    number += 2
    return number
}

print(addTwo(to: &number))  // 102
print(number)  // 102
```

함수 매개변수 타입선언 앞에 ``inout`` 을 붙이고

함수 호출 때 ``&`` 를 붙여주면 

`number`값도 동일하게 바뀌게 되는 것을 알게 되었다.

<br>

#### inout 이란 

**copy-in copy-out** 의 줄임말이며

- 함수 호출  
         ↓
- 매개변수 자리에 변수 복사
         ↓
- 함수 내부 값 수정
         ↓
- 반환한 값 변수에 재할당

         과정으로 이루어진다.


<br>


### 🚫
```swift
let letNumber = 100
addTwo(to: &letNumber) //(x)
addTwo(to: &10) //(X)
```

- 상수나 리터럴은 `inout` 매개변수에 인자값으로 전달할 수 없다.

<br>

### 참조

https://syjdev.tistory.com/21

꼼꼼한 재은씨의 swift: 문법편