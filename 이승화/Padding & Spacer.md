# Padding
---

## Default 값으로 padding 넣기

```swift
struct test: View {
    var body: some View {
        VStack {
            Text("이승화")
                .padding()
                .border(.green, width:4)
            Text("이승화")
                .border(.green, width:4)
        }
    }
}
```
이렇게 Text 하나는 Default 값으로 padding을 주고 하나는 패딩을 패딩을 주지 않고 테두리를 주면

![image](https://cdn.discordapp.com/attachments/1098858102582956064/1137997107194777640/2023-08-07_3.34.08.png)

Default 값으로 padding을 주면 모든 edge에 적용된다.

***

## 모든 테두리에 동일한 값으로 padding 넣기
```swift
struct test: View {
    var body: some View {
        VStack {
            Text("이승화")
                .padding(10)
                .border(.green, width:4)
            Text("이승화")
                .border(.green, width:4)
        }
    }
}
```

이렇게하면 모든 edge에 10만큼의 padding이 적용된다.

***

## 특정 테두리에만 padding 넣기

- edge의 종류

```swift
> - .padding(.top, 20) // 위
> - .padding(.bottom, 20) // 아래
> - .padding(.leading, 20) // 텍스트가 시작되는 지점
> - .padding(.trailing, 20) // 텍스트가 끝나는 지점
```

```swift
struct test: View {
    var body: some View {
        VStack {
            Text("이승화")
                .padding(.top,20)
                .border(.green, width:4)
            
            Text("이승화")
                .padding(.bottom,20)
                .border(.green, width:4)
            
            Text("이승화")
                .padding(.leading,20)
                .border(.green, width:4)
            
            Text("이승화")
                .padding(.trailing,20)
                .border(.green, width:4)
            
            Text("이승화")
                .border(.green, width:4)
        }
    }
}
```

![image](https://cdn.discordapp.com/attachments/1085531422468603975/1138002996857417758/2023-08-07_3.57.21.png)

이렇게 원하는 edge에 원하는 크기만큼 padding을 줄 수 있다.

***

## edge 여러개에 padding 넣기

- padding을 넣고 싶은 edge를 모두 작성해주면 된다.

```swift
struct CheckPoint3: View {
    var body: some View {
        VStack {
            Text("이승화")
                .padding([.leading, .top],20)
                .border(.green,width: 4)
            Text("이승화")
                .border(.green,width: 4)
        }
        
    }
}
```
이렇게 텍스트가 시작되는 지점과 위쪽에 padding을 주면 

![image](https://cdn.discordapp.com/attachments/1098858102582956064/1138007029114486824/2023-08-07_4.13.34.png)

짜잔 이렇게 원하는 edge에 padding을 줄 수 있다.

만약 여러개의 edge에 다른 크기로 padding을 주고 싶다면 

```swift
struct CheckPoint3: View {
    var body: some View {
        VStack {
            Text("이승화")
                .padding(EdgeInsets(top: 10, leading: 20, bottom: 40, trailing: 0))
                .border(.green,width: 4)
            Text("이승화")
                .border(.green,width: 4)
        }
        
    }
}
```
짜잔 이렇게 하면 된다!

# Spacer
---

## Spacer란?
포함하는 스택 레이아웃의 주요 축을 따라 확장되거나, 스택에 포함되지 않은 경우, 두 축 모두에서 확장되는 유연한 공간이다.

즉 Spacer는 기본적으로 사용 가능한 전체 공간을 띄워버린다

현재 Text가 갖고 있는 크기를 제외하고 남은 여백을 다 띄워버린다.

그래서 

```swift
struct CheckPoint3: View {
    var body: some View {
        HStack {
            Text("이승화")
            Spacer()
            Text("이승화")
        }
        
    }
}
```
이렇게 중간에 Spacer를 주면
![image](https://cdn.discordapp.com/attachments/1098858102582956064/1138471668512206981/2023-08-08_10.59.13.png)

이렇게 된다!
