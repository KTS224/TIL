### TIL (Today I Learned)🔥

2022-02-21


# 옵셔널 바인딩
<br>

조건문을 이용해 (let)상수 또는 (var)변수에 옵셔널값을 대입하는 방식인데

그 결과의 참 거짓 값에 따라 nil 값인지 아닌지 구분할수있다.

```swift
var optionalNumber1: Int? = 12
var optionalNumber2: Int? = nil

print(optionalNumber1) // Optional(12)
print(optionalNumber2) // nil
```
<br>

## if let

```swift
func optionalIf(_ optionalNumber: Int?) {
    if let number = optionalNumber {
        print("\(number) 반환")
    } else {
        print("값 반환 실패")
    }
}

optionalIf(optionalNumber1)  //12 반환
optionalIf(optionalNumber2)  //값 반환 실패
```
optianalNumber 를 number 에 대입하여 

대입이 가능하면 참. 따라서 if조건에맞는 값이 나오고

대입할수없으면 else 문이 실행된다.

<br>

## guard let
```swift
func optionalGuard(_ optionalNumber: Int?) {
    guard let number = optionalNumber else {
        print("값 반환 실패")
        return
    }
    print("\(number) 반환")
}

optionalGuard(optionalNumber1) //12 반환
optionalGuard(optionalNumber2) //값 반환 실패
```

guard let 은 조건에 만족하면 넘어가고

만족하지못하면 else 문이 실행된다. 