# 미디어 쿼리 사용하기

* [데모](https://ovdncids.github.io/html-css-curriculum/media-query)

## HTML 기본 구조 만들기
index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>미디어 쿼리</title>
  <link href="./index.css" rel="stylesheet">
</head>
<body>
  <div class="container">
    <ul>
      <li>아이템 1</li>
      <li>아이템 2</li>
      <li>아이템 3</li>
      <li>아이템 4</li>
      <li>아이템 5</li>
      <li>아이템 6</li>
      <li>아이템 7</li>
      <li>아이템 8</li>
      <li>아이템 9</li>
      <li>아이템 10</li>
      <li>아이템 11</li>
      <li>아이템 12</li>
    </ul>
  </div>
</body>
</html>
```

index.css
```css
body {
  margin: 0;
}
```

### ul(Unoerdered List) 태그
```css
ul {
  padding-left: 0;
}
```
* `ol`(Ordered List) 태그와 비교
* ❕ `li` 태그에 `::marker` 설명

### li 태그에 스타일 적용
```css
li {
  display: inline-block;
  width: 300px;
  height: 160px;
  background-color: #F2F2F2;
  border: 1px #DADCE0 solid;
  box-sizing: border-box;
}
```
* li 태그에 display 적용 설명
* `display: inline;`,  `display: block;`,  `display: inline-block;`,  `display: none;` 설명
* `box-sizing: border-box;`, `box-sizing: content-box;` 설명
* 화면 크기를 조절하여 아이템이 떨어지는지 확인

### 아이템 사이에 공백 제거
```diff
ul {
+ font-size: 0;
}
li {
+ font-size: 1rem;
}
```
* `ul` 태그가 `font-size: 0;` 일때 `margin` 없어지는것 확인
* 아이템 사이 공백 설명 (`li` 태그 사이에 문자 넣어 보기)

### 문서 가운데 정렬 하기
```css
.container {
  width: 1200px;
  margin: 0 auto;
  color: #4285F4;
}
```
* `margin: 0 auto;` 설명

### 미디어 쿼리 적용
```css
@media screen and (max-width: 1199px) {
  .container {
    width: 900px;
    color: #EA4335;
  }
}
```
* 미디어 쿼리 설명

```css
@media screen and (max-width: 899px) {
  .container {
    width: 600px;
    color: #FBBC05;
  }
}
```
* ❔ `max-width: 599px` 일때 `width: 300px;` 만들기
* ❔ `color: #34A853;` 수정
* <details><summary>정답</summary>

  ```css
  @media screen and (max-width: 599px) {
    .container {
      width: 300px;
      color: #34A853;
    }
  }
  ```
</details>

* 미디어 쿼리에 우선 순위 설명

## 구글 폰트 적용
https://fonts.google.com

index.html
```html
<link href="https://fonts.googleapis.com/css2?family=Gugi&display=swap" rel="stylesheet">
```
index.css
```diff
body {
+ font-family: 'Gugi', cursive;
}
```

## 과제
* ❔ `li` 태그의 `width: 200px;` 줄이고, 크기를 조절하여 아이템을 1개에서 6개까지 보여주기
