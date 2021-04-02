# 페이스북 클론

* [데모](https://ovdncids.github.io/html-css-curriculum/facebook)

## HTML 기본 구조 만들기
index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>페이스북 클론코딩</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR&display=swap" rel="stylesheet">
  <link href="./index.css" rel="stylesheet">
</head>
<body>
  <div class="wrap">
    <header></header>
    <div class="user">
      <div class="user-info"></div>
      <div class="user-menu"></div>
    </div>

    <article class="story"></article>

    <div class="post"></div>

    <div class="post"></div>

    <div class="like-comment-share"></div>

    <div class="comments"></div>

    <footer></footer>
  </div>
</body>
</html>
```

## CSS 파일 기본 설정
index.css
```css
* {
  margin: 0;
}
body {
  font-family: 'Noto Sans KR', sans-serif;
  font-size: 14px;
}
```
