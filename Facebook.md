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

## 첫번째 포스트 만들기
index.html
```diff
- <div class="post"></div>
```
```html
<div class="post">
  <div class="post-info">
    <div class="user-avatar">
      <img
        src="https://yt3.ggpht.com/ytc/AAUvwnim8ZywaqH1xNHeC9hzjC9TodC1ZNlsOu8wEuNCiw=s88-c-k-c0x00ffffff-no-rj"
        alt="Avatar"
      >
    </div>
    <div class="post-user">
      <div class="post-user-name">
        <strong>Wikitree - 위키트리</strong>
        <span class="material-icons check-icon">check_circle</span>
      </div>
      <div class="post-time">
        23시간 · <span class="material-icons">public</span>
      </div>
    </div>
    <span class="material-icons post-more">more_vert</span>
  </div>
  <div class="post-shortcut">
    연기 경력 30년 차 배우...
  </div>
  <div class="post-contents">
    <div class="post-images">
      <div class="post-images-bottom">
        <img
          width="80"
          src="https://search.pstatic.net/common/?src=http%3A%2F%2Fblogfiles.naver.net%2FMjAyMTAzMTZfMTIz%2FMDAxNjE1ODk2Nzg4OTg0.aJgztgz-aQjNulUSyI6HjZmF0W62ybu9DcHq6D85kGog.AuVKRadQnOL4fk-jI5H675COeEeghkXh8BfNWDjc3sog.JPEG.free7790%2F1.2.jpg&amp;type=sc960_832"
          alt="감우성3"
        >
      </div>
      <div class="post-images-main">
        <div>
          <img
            src="https://search.pstatic.net/common/?src=http%3A%2F%2Fimgnews.naver.net%2Fimage%2F5712%2F2021%2F03%2F18%2F0000091714_001_20210318084958753.jpg&amp;type=sc960_832"
            alt="감우성1"
          >
        </div>
        <div>
          <img
            src="https://search.pstatic.net/common/?src=http%3A%2F%2Fimgnews.naver.net%2Fimage%2F5339%2F2021%2F03%2F17%2F0000241332_001_20210317140757074.jpg&amp;type=sc960_832"
            alt="감우성2"
          >
        </div>
      </div>
      <span class="material-icons">info</span>
    </div>
    <div class="post-title">
      <div>WIKITREE.CO.KR</div>
      <strong>"결국..." '조선구마사' 최고 선배 감우성, 드디어 입 열었다 (전문)</strong>
    </div>
    <div class="post-message">
      <span><strong>이소정</strong>님이 댓글을 남겼습니다.</span>
      <span class="material-icons post-more">more_vert</span>
    </div>
  </div>
</div>
```

index.css
```css
.post-info {
  /* display: flex; */
  /* padding: 8px 8px 4px 8px; */
}
.post-user {
  /* margin-left: 8px; */
  /* flex: 1; */
}
.post-user-name, .post-user-time {
  /* display: flex; */
  /* align-items: center; */
}
.post-user-name .check-icon {
  /* color: #1A78F2; */
  /* font-size: 14px; */
  /* margin-top: 2px; */
  /* margin-left: 4px; */
}
.post-time, .post-time span {
  /* font-size: 12px; */
  /* color: #7B7A7C; */
}
.post-more {
  /* transform: rotate(90deg); */
  /* color: #5C5C5C; */
  /* height: 24px; */
}
.post-shortcut {
  /* padding: 0 8px 8px 8px; */
}
.post-images {
  /* position: relative; */
}
.post-images-main {
  /* display: flex; */
  /* font-size: 0; */
}
.post-images-main div {
  /* width: 50%; */
}
.post-images-main div:nth-child(2) {
  /* padding-left: 1px; */
}
.post-images-main div img {
  /* position: relative; */
  /* width: 100%; */
  /* height: 100%; */
}
.post-images-bottom {
  /* position: absolute; */
  /* width: 100%; */
  /* bottom: 0; */
  /* display: flex; */
  /* justify-content: center; */
}
.post-images-bottom img {
  /* position: relative; */
  /* z-index: 1; */
  /* width: 25%; */
  /* height: 25%; */
  /* border: 4px solid yellow; */
}
.post-images span {
  /* position: absolute; */
  /* top: 8px; */
  /* right: 8px; */
  /* background-color: black; */
  /* color: white; */
  /* border-radius: 50%; */
}
.post-title {
  /* border: 1px solid #F1F1F1; */
  /* background-color: #F5F6F9; */
  /* padding: 8px; */
}
.post-title div {
  /* font-size: 12px; */
  /* color: #7B7A7C; */
}
.post-title strong {
  /* font-size: 13px; */
}
.post-message {
  /* display: flex; */
  /* align-items: center; */
  /* padding: 8px; */
  /* border-bottom: 1px solid #EAEAEA; */
}
.post-message span:nth-child(1) {
  /* flex: 1; */
}
.post-image {
  /* position: relative; */
}
.post-image span {
  /* position: absolute; */
  /* right: 12px; */
  /* bottom: 12px; */
  /* background-color: #212630; */
  /* color: white; */
  /* border-radius: 50%; */
  /* padding: 4px; */
}
```
