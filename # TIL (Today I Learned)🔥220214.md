# TIL (Today I Learned)🔥
2022-02-14

# 컬랙션 타입

## Set

순서가 없고 멤버가 유일한 컬렉션 (중복 x)

```swift
var integerSet: Set<Int> = [1, 1, 2, 3, 3, 4, 5, 6]
print(integerSet) // [5, 3, 1, 6, 4, 2]
print(integerSet.sorted()) // [1, 2, 3, 4, 5, 6]
print(integerSet.count) // 6 
```
- 값의 순서는 실행마다 달라졌고
-  중복된 값은 하나로 되었다
-  만약 오름차순으로 정렬하고 싶으면 .sorted() 로 가능하다

```swift
//값 추가
integerSet.insert(100)
print(integerSet) // [5, 3, 1, 100, 6, 4, 2]
```
- 추가된 값은 제일끝이 아닌 아무곳이나 들어갔다 (실행마다 달라짐) 

```swift
//값 제거
integerSet.remove(100) //지정값제거
integerSet.removeFirst() // 가장 왼쪽값 제거
integerSet.removeAll() //다 제거
```

```swift
//반복문
for value in integerSet {
    print(value)
}
```
반복문으로 활용할 수 있을까?
고민해봐야겠다..


## Set 집합연산

```swift
let setA: Set<Int> = [1, 2, 3, 4, 5]
let setB: Set<Int> = [3, 4, 5, 6, 7]

// 합집합
let union: Set<Int> = setA.union(setB)

// 교집합
let intersection: Set<Int> = setA.intersection(setB)

// 차집합
let subtractiong: Set<Int> = setA.subtracting(setB)
```