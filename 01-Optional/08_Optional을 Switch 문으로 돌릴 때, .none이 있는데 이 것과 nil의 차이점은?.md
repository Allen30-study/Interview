## Optional을 Switch 문으로 돌릴 때, .none이 있는데 이 것과 nil의 차이점은?
- 차이점은 없고 완전히 동일한 개념이다. Enum 타입인 임시값의 형태를 담아두는 개념이다.
```swift
let optionalValue: Int? = nil

// 사용 방법 1: nil
if optionalValue == nil {
    print("Optional is nil")
} else {
    print("Optional has a value")
}

// 사용 방법 2: .none
switch optionalValue {
case .none:
    print("Optional is nil")
case .some(let value):
    print("Optional has a value: \(value)")
}
```