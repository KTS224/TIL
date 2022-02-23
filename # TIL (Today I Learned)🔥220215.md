# TIL (Today I Learned)🔥
2022-02-15

## Array

- 순서를 갖고 중복이 가능하다
- 빈 배열을 만들때는 반드시 타입을 명시해야한다
- 순서를 인덱스라고 하며 0부터 시작한다


```swift
var animal: Array<String> = Array<String>()
```

### 추가 
```swift
animal.append("tiger")
//["tiger"]
animal.append(contentsOf: ["lion, elephant"])
//["tiger", "lion", "elephant"]
animal.insert("monkey", at: 2)
//["tiger", "lion", "monkey", "elephant"]
animal.insert(contentsOf: ["lion2, elephant2"], at: 2)
//["tiger", "lion", "lion2", "elephant2", "monkey", "elephant"]
```



### 교체
```swift
animal[0...3] = ["dog"]
//["dog", "monkey", "elephant"]
animal.replaceSubrange(1...2, with: ["cat"])
//["dog", "cat"]
```


### 삭제
```swift
animal.remove(at: 0)
//["cat"]
animal.removeAll()
//[]
```

```swift
//개수 판별 가능
animal.count == 0 
//true 또는 false 값으로 판별 가능 

animal.isEmpty // 비어있는지 true false
```