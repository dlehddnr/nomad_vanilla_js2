# Vanilla Js 2

## JS part

### Canvas Events
- clientX,Y 는 이 윈도우 전체의 범위 내에서 마우스의 위치값을 나타낸다.
- offsetX,Y 는 canvas태그 내에 범위에서 마우스의 위치값.
- mousedown, mouseup, mousemove, mouseleave 작성.

### Canvas MDN
- canvas 는 context를 갖는 HTML요소이다, 그건 우리가 픽셀에 접근 할 수 있는 방법이다.
- 다시한번! context는 canvas 안에서 픽셀을 다루는 것이다.
- path 를 만드는 건 기본적으로 선, 선의 시작점을 만드는 것!
- 시작점은 마우스가 움직이는 곳이라면 어디든 OK!
- 하지만 클릭하고 나면 시작점부터 클릭한 곳 까지 라인을 만든다.
  
- Canvas 는 사이즈를 가져야한다. canvas 는 두개의 사이즈를 가지는데 css size, pixel manipulating size

```canvas.width = 700; canvas.height = 700;```
- 선 설정

```ctx.strokeStyle = "#2c2c2c"; ctx.lineWidth = 2.5;```

- [x] 선을 만드는 과정은 2.2 Recap을 참조하도록 하자.

### Change Color
- Array.from 메소드는 object로 부터 array를 만든다.
```
Array.from(colors).forEach(color =>
  color.addEventListener("click", handleColorClick)
);
```
로 colors라는 elementsByClassName 으로 받아온 array를 각각 eventListen시켜주고

```
function handleColorClick(event) {
  const color = event.target.style.backgroundColor;
  ctx.strokeStyle = color;
}
```
클릭하면 타겟 스타일의 배경색으로 스트로크스타일을 바꾸어 준다.

### Brush Size
range 이벤트는 input에 반응한다.

### Fill
Fill 클릭 -> 색 클릭 -> 캔버스 클릭 -> 색으로 가득 채우기.

### fillRect
ctx.fillRect(x좌표, y좌표, 가로, 세로)
fillStyle로 색 지정 가능하다.
fillStyle을 바꿔도 그 앞에 미리 그린 사각형에는 영향이 가지 않는다.

### Small Bug
그리고 이미지를 저장하면 배경이 tansparent(투명하다), 실제 canvas의 배경색을 설정하지 않았기때문.
HTML 엘리먼트의 배경색만 지정해줌.

### download
```
<a href="#">
```
대신에 <a download="#">이런식으로 써줄 수 있다.
다운로드 받을때 href = 이미지 여야 하고
            download = 이름 을 가져와야 한다.