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
    <div class="user"></div>

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

* [구글 폰트](https://fonts.google.com/)

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

## 사용자 정보 만들기
index.html
```diff
- <div class="user"></div>
```
```html
<div class="user">
  <div class="user-info">
    <div class="user-avatar">
      <img
        height="24"
        src="https://www.w3schools.com/howto/img_avatar.png"
        alt="Avatar"
      >
    </div>
    <div class="user-question">
      <span>무슨 생각을 하고 계신가요?</span>
    </div>
  </div>
  <div class="user-menu">
    <div class="user-menu-live">
      <span class="material-icons">missed_video_call</span>
      <strong>라이브</strong>
    </div>
    <div class="user-menu-picture">
      <span class="material-icons">image</span>
      <strong>사진</strong>
    </div>
    <div class="user-menu-group">
      <span class="material-icons">videocam</span>
      <strong>영상톡 모임</strong>
    </div>
  </div>
</div>
```
index.css
```css
.user-info {
  /* display: flex; */
  /* border-bottom: 2px solid #EAEAEA; */
  /* padding: 8px; */
}
.user-avatar, .user-question {
  /* display: flex; */
  /* align-items: center; */
}
.user-avatar img {
  /* width: 36px; */
  /* height: 36px; */
  /* border-radius: 50%; */
}
.user-question {
  /* margin-left: 8px; */
}

.user-menu {
  /* display: flex; */
  /* margin-top: 4px; */
  /* margin-bottom: 4px; */
}
.user-menu-live, .user-menu-picture, .user-menu-group {
  /* flex: 1; */
  /* display: flex; */
  /* justify-content: center; */
  /* align-items: center; */
  /* padding: 4px; */
}
.user-menu-picture {
  /* border-left: 2px solid #EAEAEA; */
  /* border-right: 2px solid #EAEAEA; */
}
.user-menu span {
  /* font-size: 16px; */
}
.user-menu strong {
  /* margin-left: 4px; */
  /* font-size: 12px; */
}
.user-menu-live span {
  /* color: #F10140; */
}
.user-menu-picture span {
  /* color: #36B74C; */
}
.user-menu-group span {
  /* color: #8252ED; */
}
```

## 스토리 만들기
index.html
```diff
- <article class="story"></article>
```
```html
<article class="story">
  <section>
    <img
      width="100" height="150"
      src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRJfWmYaMeclyRtrJXHIIFtXKIn9QsXQQ4T94q-uySZVnclTylRT7yt1CKWpFVXru06HuI&amp;usqp=CAU"
      alt="Nature"
    >
    <img
      class="kakao"
      height="120"
      src="./images/kakao-emoticon.png"
      alt="Kakao"
    >
    <div class="cover"></div>
    <span class="material-icons add-circle">add_circle</span>
    <span class="story-make">스토리 만들기</span>
  </section>
  <section>
    <img
      width="100" height="150"
      src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRQJh10fVzAuq4zlqL2RnCAiPVaifX0l8WtMQ&amp;usqp=CAU"
      alt="Nature"
    >
    <img
      class="account-circle" width="28" height="28"
      src="https://www.nicepng.com/png/full/136-1366211_group-of-10-guys-login-user-icon-png.png">
    <span class="story-name">신승환</span>
  </section>
  <section>
    <img
      width="100" height="150"
      src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSm60W0DcB3-N6bxvv2he1yvkU-Th09g_cRbUOe34YVsbC7yLK_0Gs5n4gzshna9dx_jYo&amp;usqp=CAU"
      alt="Nature"
    >
    <img
      class="account-circle" width="28" height="28"
      src="https://www.nicepng.com/png/full/136-1366211_group-of-10-guys-login-user-icon-png.png">
    <span class="story-name">임지훈</span>
  </section>
  <section>
    <img
      width="100" height="150"
      src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSfDHPkuaPFWCWh0RjgFofWKczjH9gKCPodnPVPRccfqLhwEi1hgUPhjjznIaKsjP3JG-Y&amp;usqp=CAU"
      alt="Avatar"
    >
    <img
      class="account-circle" width="28" height="28"
      src="https://i.pinimg.com/originals/06/a5/58/06a558f03667345ce97315f3de4afbaf.jpg">
    <span class="story-name">Eh Bee</span>
  </section>
</article>
```

* [카카오 이모티콘](https://ovdncids.github.io/html-css-curriculum/facebook/images/kakao-emoticon.png)

index.css
```css
.story {
  /* display: flex; */
  /* border-top: 7px solid #BEBFC6; */
  /* border-bottom: 7px solid #BEBFC6; */
  /* padding: 4px; */
  /* overflow: hidden; */
}
.story section {
  /* position: relative; */
  /* padding: 4px; */
}
.story section img {
  /* border-radius: 12px; */
}
.story .kakao {
  /* position: absolute; */
  /* top: -20px; */
  /* left: 14px; */
  /* z-index: 1; */
}
.story .story-make {
  /* position: absolute; */
  /* top: 130px; */
  /* left: 18px; */
  /* font-size: 12px; */
}
.story .cover {
  /* height: 50px; */
  /* background-color: #F5F6F9; */
  /* position: absolute; */
  /* width: 100px; */
  /* top: 105px; */
  /* border-radius: 0 0 12px 12px; */
}
.story .add-circle {
  /* position: absolute; */
  /* top: 88px; */
  /* left: 38px; */
  /* background-color: #F5F6F9; */
  /* border-radius: 50%; */
  /* font-size: 36px; */
  /* color: #1A78F2; */
}
.story .account-circle {
  /* position: absolute; */
  /* top: 8px; */
  /* left: 8px; */
  /* background-color: #1A78F2; */
  /* padding: 4px; */
  /* border-radius: 50%; */
}
.story .story-name {
  /* position: absolute; */
  /* top: 130px; */
  /* left: 12px; */
  /* color: white; */
  /* font-size: 12px; */
}
```
