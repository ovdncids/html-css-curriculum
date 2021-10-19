# CSS 우선순위
* [데모](https://ovdncids.github.io/html-css-curriculum/priority-css)

## HTML
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>CSS 우선 순위</title>
    <link href="./index.css" rel="stylesheet">
  </head>
  <body>
    <ul class="tag-ul">
      <li class="tag-li-first">과일</li>
      <li><a href="https://naver.com" class="animal">동물</a></li>
      <li><a href="https://google.com" id="people">사람</a></li>
      <li>하늘</li>
    </ul>
  </body>
</html>
```

## CSS
### 모든것(*): 0점
```css
* {
  padding: 4px;
}
* {
  padding: 8px;
}
```
* 나중에 선언된 CSS가 우선순위가 높다

### 태그이름: 1점
```css
body {
  background-color: red;
}
body {
  background-color: white;
}
```

### 클래스명(.class): 10점
```css
.tag-ul {
  background-color: orange;
}
ul {
  background-color: white;
}
```

### 가상클래스속성(:속성명): 10점
```css
li:first-child {
  background-color: yellow;
}
.tag-li-first {
  background-color: white;
}
```
* ❔ 문제: `.tag-li-first`를 우선순위로 보이려면

### 속성선택자([href]): 10점
```css
.animal {
  background-color: green;
}
[href*="https://naver"] {
  background-color: white;
}
```
* ❔ 문제: `.animal`을 우선순위로 보이려면

### id(#): 100점
```css
a#people {
  background-color: lime;
}
/*
 * :link는 :visited 이전 상황이다
 * :visited 이후에 크롬에서 방문기록을 삭제 하면, :link를 다시 볼 수 있다
 * 개발자 도구에서는 :link로 되어 있지만, :visited이 보이고 있을 수 있다
 * :active는 마우스 다운을 뜻 한다
 */
a#people:link {
  color: red;
  text-decoration: none;
  background-color: white;
}
a#people:visited {
  color: orange;
  background-color: black;
}
a#people:hover {
  color: green;
  background-color: silver;
}
a#people:active {
  color: purple;
  background-color: aqua;
}
```

### style속정: 1000점
```diff
- <li>하늘</li>
```
```html
<li style="background-color: pink;">하늘</li>
```

### !important: 최고점
```css
li a {
  background-color: skyblue !important;
}
```

## 점수표
| 지정방법 | 예제 | 점수 |
|---|:---|:---|
| !important | !important | 최고점 |
| 직접기입 | style="" | 1000점 |
| ID | #sample | 100점 |
| Class | .sample | 10점 |
| 속성선택자 | a[href*="sample"] | 10점 |
| 가상클래스속성 | :first-child | 10점 |
| 태그선택자 | ul | 1점 |
| 전체선택 | *  | 0점 |
