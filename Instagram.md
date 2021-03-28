# 인스타그램 클론

* [데모1](https://ovdncids.github.io/html-css-curriculum/instagram)
* [데모2](https://ovdncids.github.io/html-css-curriculum/instagram/index2.html)

## HTML 기본 구조 만들기
index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>인스타그램 클론코딩</title>
  <link href="./index.css" rel="stylesheet">
</head>
<body>
  <div class="wrap">
    <header></header>
    <div class="user">
      <div class="user-info"></div>
      <div class="user-description"></div>
      <div class="user-menu"></div>
    </div>
    <article>
      <div class="article-menu"></div>
      <div class="article-contents"></div>
    </article>
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
  background-color: black;
  color: white;
  font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;
  font-size: 14px;
}
```

## Icons 및 이미지 파일
icons.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Google Material Icons</title>
  <link href="https://fonts.googleapis.com/css2?family=Material+Icons" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Material+Icons+Outlined" rel="stylesheet">
</head>
<body>
  <div>
    <span class="material-icons">arrow_back_ios_new</span>
    <span class="material-icons">check_circle</span>
    <span class="material-icons">notifications_none</span>
    <span class="material-icons">more_vert</span>
    <span class="material-icons">expand_more</span>
    <span class="material-icons">grid_on</span>
    <span class="material-icons">live_tv</span>
    <span class="material-icons-outlined">perm_contact_calendar</span>
    <span class="material-icons">play_arrow</span>
    <span class="material-icons">content_copy</span>
    <span class="material-icons-outlined">home</span>
    <span class="material-icons">search</span>
    <span class="material-icons-outlined">shop</span>
    <span class="material-icons-outlined">shopping_bag</span>
    <span class="material-icons-outlined">account_circle</span>
    <div class="avatar">
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
    </div>
  </div>
</body>
</html>
```
https://material.io/resources/icons/?style=baseline

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
  <div class="header-back">
    <span class="material-icons">arrow_back_ios_new</span>
  </div>
  <div class="header-title">
    <strong>Name</strong>
    <span class="material-icons header-check-icon">check_circle</span>
  </div>
  <div class="header-memu">
    <span class="material-icons">notifications_none</span>
    <span class="material-icons">more_vert</span>
  </div>
</header>
```

index.css
```css
header {
  /* display: flex; */
  /* padding: 8px; */
}
.header-title {
  /* flex: 1; */
  /* display: flex; */
  /* justify-content: center; */
  /* align-items: center; */
}
.header-check-icon {
  /* color: #3697EF; */
  /* font-size: 12px; */
  /* margin-top: 4px; */
}
```
* ❔ `Name`과 `check_circle 아이콘` 간격 띄우기

## 회원 정보 만들기
index.html
```diff
- <div class="user-info"></div>
```
```html
<div class="user-info">
  <div class="user-avatar">
    <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
  </div>
  <div class="user-count-post">
    <strong>571</strong>
    <span>게시판</span>
  </div>
  <div class="user-count-follower">
    <strong>1,909만</strong>
    <span>팔로워</span>
  </div>
  <div class="user-count-following">
    <strong>111</strong>
    <span>팔로잉</span>
  </div>
</div>
```

index.css
```css
.user-info {
  /* display: flex; */
  /* padding: 8px; */
}
.user-avatar, .user-count-post, .user-count-follower, .user-count-following {
  /* flex: 1; */
  /* display: flex; */
  /* flex-direction: column; */
  /* justify-content: center; */
  /* align-items: center; */
}
.user-avatar {
  /* position: relative; */
  /* width: 80px; */
  /* height: 80px; */
}
.user-avatar img {
  /* width: 70px; */
  /* height: 70px; */
  /* position: absolute; */
  /* left: 5px; */
  /* top: 5px; */
  /* border-radius: 50%; */
}
.user-avatar::after {
  content: '';
  /* border: 2px solid #3F3F3F; */
  /* width: 80px; */
  /* height: 80px; */
  /* position: absolute; */
  /* left: 0; */
  /* top: 0; */
  /* border-radius: 50%; */
  /* box-sizing: border-box; */
}
```

## 회원 설명 만들기
index.html
```diff
- <div class="user-description"></div>
```
```html
<div class="user-description">
  <p>
    이지금 IU<br>
    Celebrity ⭐💛💛💛💛<br>
    youtu.be/O-q1KalFCLU<br>
    dustziii_님, stehzlla4님 외 52명이 팔루우합니다.<br>
    번역 보기
  </p>
</div>
```

index.css
```css
.user-description {
  padding: 8px;
}
```

## 회원 메뉴 만들기
index.html
```diff
- <div class="user-menu"></div>
```
```html
<div class="user-menu">
  <div class="user-menu-following">
    팔로잉<span class="material-icons">expand_more</span>
  </div>
  <div class="user-menu-message">
    메시지
  </div>
  <div class="user-menu-more">
    <span class="material-icons">expand_more</span>
  </div>
</div>
```

index.css
```css
.user-menu {
  /* display: flex; */
  /* padding: 8px; */
}
.user-menu-following, .user-menu-message, .user-menu-more {
  /* border: 2px solid #3F3F3F; */
  /* display: flex; */
  /* justify-content: center; */
  /* align-items: center; */
  /* border-radius: 4px; */
}
.user-menu-following, .user-menu-message {
  /* flex: 1; */
  /* margin-right: 4px; */
}
```

## 본문 메뉴 만들기
index.html
```diff
- <div class="article-menu"></div>
```
```html
<div class="article-menu">
  <div class="article-menu-grid active">
    <span class="material-icons">grid_on</span>
  </div>
  <div class="article-menu-tv">
    <span class="material-icons">live_tv</span>
  </div>
  <div class="article-menu-contact">
    <span class="material-icons">perm_contact_calendar</span>
  </div>
</div>
```

index.css
```css
.article-menu {
  /* display: flex; */
}
.article-menu-grid, .article-menu-tv, .article-menu-contact {
  /* flex: 1; */
  /* display: flex; */
  /* justify-content: center; */
  /* align-items: center; */
  /* padding: 8px; */
}
.article-menu-grid.active, .article-menu-tv.active, .article-menu-contact.active {
  /* border-bottom: 1px solid white; */
}
```

## 본문 만들기
index.html
```diff
- <div class="article-contents"></div>
```
```html
<div class="article-contents">
  <div class="article-contents-row">
    <section>
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
      <span class="material-icons">play_arrow</span>
    </section>
    <section>
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
      <span class="material-icons">play_arrow</span>
    </section>
    <section>
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
      <span class="material-icons">play_arrow</span>
    </section>
  </div>
  <div class="article-contents-row">
    <section>
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
      <span class="material-icons">content_copy</span>
    </section>
    <section>
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
      <span class="material-icons">content_copy</span>
    </section>
    <section>
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
      <span class="material-icons">content_copy</span>
    </section>
  </div>
  <div class="article-contents-row">
    <section>
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
      <span class="material-icons">content_copy</span>
    </section>
    <section>
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
      <span class="material-icons">content_copy</span>
    </section>
    <section>
      <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar">
      <span class="material-icons">content_copy</span>
    </section>
  </div>
</div>
```

index.css
```css
.article-contents-row {
  /* display: flex; */
  /* font-size: 0; */
}
.article-contents-row section {
  /* margin: 1px; */
  /* position: relative; */
  /* width: 100%; */
}
.article-contents-row section img {
  /* width: 100%; */
}
.article-contents-row section span {
  /* position: absolute; */
  /* right: 8px; */
  /* top: 8px; */
}
```

## Footer 만들기
index.html
```diff
- <footer></footer>
```
```html
<footer>
  <div><span class="material-icons-outlined">home</span></div>
  <div><span class="material-icons">search</span></div>
  <div><span class="material-icons-outlined">shop</span></div>
  <div><span class="material-icons-outlined">shopping_bag</span></div>
  <div><span class="material-icons-outlined">account_circle</span></div>
</footer>
```

index.css
```css
footer {
  /* position: fixed; */
  /* bottom: 0; */
  /* display: flex; */
  /* padding: 8px; */
  /* border-top: 2px solid #050505; */
  /* width: 100%; */
  /* background-color: black; */
}
footer div {
  /* flex: 1; */
  /* display: flex; */
  /* justify-content: center; */
  /* align-items: center; */
}
```

### 이미지 짤리는 부분 보이기
```css
article {
  margin-bottom: 42px;
}
```

## 본문 메뉴 밑줄 길이 맞추기
```css
.article-menu-grid, .article-menu-tv, .article-menu-contact {
  ...
  margin: 1px;
}
```

## 과제
* [데모2](https://ovdncids.github.io/html-css-curriculum/instagram/index2.html) 만들어 보기
