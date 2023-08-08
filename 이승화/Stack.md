# Stack

## Stack은 어떨 때 쓸까?
- body라는 프로퍼티의 타입이 some View, 즉 불투명타입(Opaque Type)이라서 내부에서 View를 준수하고 있는 객체면 어떤 객체든 리턴이 가능하지만, 단 한개의 View만 리턴을 해야한다!

- 그럴 때 쓰는게 바로 Stack

## VStack
- VStack(Vertical Stack)은 자식들을 수직으로 배열하는 뷰이다.
```swift
var body: some View {
        VStack {
            Text("이")
            Text("승")
            Text("화")
        }
    }
```
이렇게 Text라는 View를 VStack으로 감싸면 
![image](https://cdn.discordapp.com/attachments/1098858102582956064/1137986157486026772/2023-08-07_2.50.34.png)
이렇게 수직으로 배열이 된다!

***

- VStack은 alignment, spacing을 설정해줄 수 있으며, alignment의 디폴트는 center로 되어 있다.

- VStack의 alignment는 leading, center, trailing이 있다.
```swift
var body: some View {
        VStack(alignment: .leading) {
            Text("치즈")
            Text("베이글")
            Text("🥯")
        }
    }
```
![image](https://cdn.discordapp.com/attachments/1098858102582956064/1138450518923026442/image.png)

***

- 또한 Text처럼 배경색, 패딩, 테두리 등 여러가지 설정을 해줄 수 있다!!
```swift
 var body: some View {
        VStack {
            Text("이")
            Text("승")
            Text("화")
        }
            .background(.green)
            .padding()
            .border(.gray, width:4)
    }
```
![image](https://cdn.discordapp.com/attachments/1098858102582956064/1137988338796728320/2023-08-07_2.59.16.png)

***

## HStack 

- HStack(Horizontal Stack)은 자식들을 수평으로 배열하는 뷰이다.
```swift
var body: some View {
        HStack {
            Text("이")
            Text("승")
            Text("화")
        }
    }
```
이렇게 Text라는 View를 HStack으로 감싸면 
![image](https://cdn.discordapp.com/attachments/1098858102582956064/1137989320930770976/2023-08-07_3.02.40.png)
이렇게 수평으로 배열이 된다!

*** 

- HStack도 VStack과 사용법은 똑같지만 HStack은 alignment가 top, center, bottom이 있다

- 그래서 이렇게 alignment를 leading으로 주게 되면 오류가 뜬다!!
![image](https://cdn.discordapp.com/attachments/1098858102582956064/1138451887633473636/image.png)

***

- HStack도 마찬가지로 배경색, 패딩, 테두리 등 여러가지 설정을 해줄 수 있다.
```swift
var body: some View {
        HStack {
            Text("이")
            Text("승")
            Text("화")
        }
            .background(.green)
            .padding()
            .border(.gray, width:4)
    }
```
![image](https://cdn.discordapp.com/attachments/1098858102582956064/1137990916813111296/2023-08-07_3.09.31.png)

***

## ZStack
- ZStack은 자식들을 오버레이하고 두 축으로 배열하는 뷰이다.

- ZStack은 먼저 선언해주는 View일 수록 겹쳐졌을 때 뒤에 배치된다.
```swift
var body: some View {
        HStack {
            Text("이")
            Text("승")
            Text("화")
        }
}
```
![image](https://cdn.discordapp.com/attachments/1098858102582956064/1137993416102391808/2023-08-07_3.19.28.png)