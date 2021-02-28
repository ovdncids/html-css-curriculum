# Position 속성

* [데모](https://ovdncids.github.io/html-css-curriculum/position)

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
    <link href="./index3.css" rel="stylesheet">
    <title>HTML 기본 구조</title>
  </head>
  <body>
    <div class="static">static1</div>
    <div class="parent">
      <div class="relative">relative</div>
      <div class="static">static2</div>
      <div class="absolute">absolute</div>
      <div class="static">static3</div>
      <div class="fixed">fixed</div>
    </div>
    <div class="static">static4</div>
  </body>
</html>
```
position.css
```css
body {
  color: white;
}

.parent {
  position: static;
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
  position: absolute;
  background: #EA4335;
  width: 100px;
  height: 100px;
}

.fixed {
  position: fixed;
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

❔ `.static` class에 `top: 50px;` `left: 50px;` `z-index: 100;` 적용

## relative
```css
position: relative;
```
`top, right, bottom, left` 위치를 변경 하여도, 문서 안에서 자신의 영역 크기를 유지한다.

`z-index: 0;` 보다 작지 않으면 항상 `position: static;` 보다 위에 보이게 된다

❔ `.relative` class에 `top: 50px;` `left: 50px;` 적용

❔ `top: 150px;` 값을 100씩 늘리기

❔ `z-index: 1;` 적용

❔ `z-index: -1;` 적용

## absolute
```css
position: absolute;
```
문서 안에서 자신만에 영역을 유지 하지 않는다.

기본 위치는 자신의 바로 위에 엘리먼트 다음에 위치 한다.

조상이 모두 `position: static;`일 경우: `top, right, bottom, left` 위치는 문서 최상단이 된다.

조상이 `position: static;`이 아닐 경우: 해당 조상 기준으로 `top, right, bottom, left` 위치가 결정 된다.

❔ `.absolute` class에 `top: 50px;` `left: 50px;` 적용

❔ `top: 150px;` 값을 100씩 늘리기

❔ `z-index: 1;` 적용

❔ `z-index: -1;` 적용

❔ `.absolute` class에 `position: relative;`,  `position: absolute;` 적용

## fixed
```css
position: fixed;
```
absolute와 비슷하지만 차이점은 조상과 상관 없이 `top, right, bottom, left` 위치는 문서 최상단이 된다.

❔ `.fixed` class에 `top: 50px;` `left: 50px;` 적용

❔ `top: 150px;` 값을 100씩 늘리기

❔ `z-index: 1;` 적용

❔ `z-index: -1;` 적용

❔ `.absolute` class에 `position: relative;`,  `position: absolute;` 적용
