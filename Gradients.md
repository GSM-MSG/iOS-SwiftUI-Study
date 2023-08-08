# <b> Gradients </b>
그라데이션을 지정해주는 기능입니다.  
Linear, Angular, Radial로 3가지 종류로 나누어집니다.

<br>

<hr>

<br>

## <b> Linear Gradients </b>
- 색상입력 - colors  
- 시작지점 - startPoint  
- 종료지점 - endPoint  

<br>

UnitPoint는 9가지의 지점이 있습니다.
![](https://blog.kakaocdn.net/dn/bNAAo9/btrOyBD28R2/0MJd1e2bz3GlO5We8Y24z1/img.png)

<br>

```Swift
LinearGradient(colors: [.pink, .red], startPoint: .topTrailing, endPoint: .bottomLeading)
  .overlay(Text("LenarGradient"))
```
- 오른쪽 위에서 부터 핑크색이 시작되어서 왼쪽 아래로 갈수록 빨간색이 되는 그라데이션

<br>

<hr>

<br>

## <b> Radial Gradients </b>
- 색상 입력 - colors  
- 중앙 지점 - center  
- 시작 각도 - startRadius  
- 종료 각도 - endRadius

<br>

```Swift
RadialGradient(colors: [.pink, .red], center: .center, startRadius: 0, endRadius: 270)
  .overlay(Text("RadialGradient"))
```

- 가운데 핑크부분으로 시작되어서 바깥쪽으로 갈수록 빨간색이 되는 그라데이션

<br>

<hr>

<br>

## <b> AngularGradient </b>
- 색상 입력 - colors
- 중앙 지점 - center

<br>

```Swift
AngularGradient(colors: [.pink, .red], center: .center)
  .overlay(Text("AngularGradient"))
```

- 오른쪽 중앙 핑크부분에서 시작되어서 시계방향으로 가면서 빨간색이되는 그라데이션