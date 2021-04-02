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

## Header 만들기
index.html
```html
<link href="https://fonts.googleapis.com/css2?family=Material+Icons" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Material+Icons+Outlined" rel="stylesheet">
```
```diff
- <header></header>
```
```html
<header>
  <div class="header-title">
    <img
      src="https://w.namu.la/s/973378361c71397a08ab94a2c22e810a78cd676aac0e9f3db0c3c95698947574541e9191b623365b6149a706e0128fa5e35183fdbcd247efaf0fe486caa4c57a2e24ae2afe0e353614503b0d620a46980cc29e4c889f01a5e901d8fa3ce09673"
      height="24"
      alt="facebook-log"
    >
  </div>
  <div class="header-memu">
    <span class="material-icons">search</span>
    <span class="material-icons">offline_bolt</span>
  </div>
</header>
```

index.css
```css
header {
  /* display: flex; */
  /* padding: 8px; */
  /* border-bottom: 1px solid #F1F1F1; */
}
.header-title {
  /* flex: 1; */
  /* display: flex; */
  /* align-items: center; */
}
.header-memu span {
  /* background-color: #DFE0E6; */
  /* padding: 4px; */
  /* border-radius: 50%; */
}
```
