# TIL (Today I Learned)🔥
2022-02-18

# 튜플

한 가지 타입의 아이템만 저장할 수 있는 배열이나 딕셔너리와는 달리 

하나의 튜플에 여러 가지 타입의 아이템을 저장할 수 있지만

배열이나 집합과 달리 소괄호()를 사용하여 정의한다.

```swift
var tuple = ("zero", 3, 2, "three")
```

```swift
tuple.0 // zero
tuple.1 // 1
tuple.2 // 2
tuple.3 // three
```


튜플안의 튜플의 값을 접근할 수도 있다.

### 튜플속 튜플

```swift
var tuple = ("zero", 3, 2, "three")
var otherTuple = ((tuple), 4, 5)
```

```swift
otherTuple.0 // ("zero", 1, 2, "three")
otherTuple.0.0 // zero
otherTuple.0.1 // 1
otherTuple.1 // 4
otherTuple.2 // 5
```
### 이름 붙히기
```swift
var namedTuple = (age: 50, place: ["cafe, home"]) // (age: 50, place: ["cafe, home"])
// namedTuple = ("lol", ["playground", "school"])  (X)
// age 값이 Int 값이었으므로 String 타입으로 변경이 불가능하다
namedTuple.age // 50
namedTuple.place // ["cafe, home"]
```
- 이름을 붙여서 이름으로 값에 접근할 수 있다.

- 선언하고 나면 같은 타입 값으로 만 바꿀 수 있다.

- 값의 추가나 삭제는 할 수 없다.


#### 참조

https://zeddios.tistory.com/238

https://docs.swift.org/swift-book/ReferenceManual/Types.html