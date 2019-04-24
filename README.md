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