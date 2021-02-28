# Position 속성

## z-index
모든 속성의 기본 z-index 값은 0이다

<!-- 구글 색상
파란색: #4285F4
빨간색: #EA4335
노란색: #FBBC05
녹색: #34A853 -->

position.html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <link href="./position.css" rel="stylesheet">
    <title>Position 속성</title>
  </head>
  <body>
    <div class="static" id="container">
      <div class="static">static</div>
      <div class="relative">relative</div>
      <div class="static">static</div>
      <div class="absolute">absolute</div>
      <div class="static">static</div>
      <div class="fixed">fixed</div>
      <div class="static">static</div>
    </div>
  </body>
</html>
```
position.css
```css
div {
  color: white;
}

.static {
  background: #4285F4;
  width: 100px;
  height: 100px;
}

.relative {
  position: relative;
  background: #FBBC05;
  width: 100px;
  height: 100px;
}

.absolute {
  position: relative;
  background: #EA4335;
  width: 100px;
  height: 100px;
}

.fixed {
  position: relative;
  background: #34A853;
  width: 100px;
  height: 100px;
}
```

## static
```css
position: static;
```
기본 속성으로 position을 지정하지 않으면 `position: static;`이 된다.

`top, right, bottom, left, z-index` 값을 수정은 되지만 적용이 되지 않는다.

**static을 제외한 모든 position값은 `top, right, bottom, left, z-index` 값을 수정하면 바로 적용 된다.**

❔ `.static` class에 `top: 50px;` `left: 50px;` `z-index: 100;` 적용하기

## relative
```css
position: relative;
```
`top, right, bottom, left` 위치를 변경 하여도 자신의 영역 크기를 유지한다.

`z-index: 0;` 보다 작지 않으면 항상 `position: static;` 보다 위에 보이게 된다

❔ `.relative` class에 `top: 50px;` `left: 50px;` 적용하기

❔ `top: 50px;` 값을 100씩 늘려 보기

❔ `z-index: 1;` 적용 하기

❔ `z-index: -1;` 적용 하기


