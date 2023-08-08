# <b> Color </b>
원하는 색상을 지정해주면 그 색으로 변경해주는 기능입니다.

<br>

<hr>

<br>

## <b> Color </b>  
Color.색상을 해주게 되면 원하는 색으로 바뀝니다.

```
Color.primary
```
- Color.primary는 라이트 모드일 때 검정색, 다크모드일 때는 흰색으로 변합니다.

<br>

<hr>

<br>

## <b> UIColor </b>
Color에서 제공되지 않는 다양한 색들을 가지고있습니다.  
<b> ex )</b> systemGray같은 것들을 제공합니다.

``` 
Color(UIColor.secondarySystemBackground)
```
- UIColor.secondarySystemBackground는 라이트모드일 때 옅은 회색, 다크모드일 때는 진한 회색으로 바뀝니다.

<br>

<hr>

<br>

## <b> 사용자 정의 컬러 만들기 </b>
1. Asset에서 오른쪽 클릭 또는 하단의 +버튼을 누른뒤 New Color Set을 선택 해 줍니다.
2. Color Set이 생성되면 라이트모드, 다크모드에서 사용할 색상을 각각 정해줍니다.
3. 인스펙터 창을 열고, Show Color Panel을 누르면 다양한 방식으로 원하는 색상을 만들 수 있습니다.
4. Color("색상이름")을 해주면 라이트모드, 다크모드일 때 지정해둔 색깔 그대로 나옵니다.

```
Color("IsNotBanana")
```

<br>

<hr>

<br>

## <b> Shadow </b>
그림자 효과를 줄 수 있는 기능입니다.

```
.shadow(radius: 10)
```
그림자 색상과 위치도 radius로 정해줄 수 있습니다.