# HTML & CSS

# Flex 사용하여 레이아웃 잡기

* [데모](https://ovdncids.github.io/html-css-curriculum/flex)

## HTML 기본 구조 만들기
index.html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>HTML 기본 구조</title>
  </head>
  <body>
  </body>
</html>
```

## div, span 태그 설명
```html
  <body>
    <div>div 태그 설명</div>
    <span>span 태그 설명</span>
  </body>
```

## nav, ul, li, h1 태그 설명
```html
  <body>
    <div class="wrap">
      <nav>
        <ul>
          <li><h1>⛪</h1></li>
          <li><h1>🎡</h1></li>
          <li><h1>🎠</h1></li>
          <li><h1>🎮</h1></li>
          <li><h1>📷</h1></li>
          <li><h1>📼</h1></li>
        </ul>
      </nav>
    </div>
  </body>
```
**이모지**
https://www.emojiengine.com/ko/

## section, header 태그 설명
```html
    <div class="wrap">
      ...

      <section>
        <header>
          <div><h2>⛪</h2></div>
          <div><h2>🤖</h2></div>
        </header>
        <div class="contents">
          <div><h3>Home</h3></div>
        </div>
      </section>
```

## css 파일 연결 하기
```html
  <head>
    <link href="./index.css" rel="stylesheet">
```

index.css
```css
body {
  margin: 0;
}

h1, h2, h3 {
  margin: 0;
}
```
**margin 설명**

## border, padding, list-style-type 설명
```css
nav {
  border-right: 1px lightgray solid;
}

ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

ul li {
  padding: 1rem;
}
```

## flex 설명 & 가로 정렬
```css
.wrap {
  display: flex;
}
section {
  flex: 1;
}
```

## section 세로 정렬 하기
```css
section {
  flex: 1;
  display: flex;
  flex-direction: column;
}
```

## header 좌우 정렬 하기
```css
header {
  display: flex;
  padding: 1rem;
  border-bottom: 1px lightgray solid;
}

header div:first-child {
  flex: 1;
}
```

## contents 가운데 정렬 하기
```css
.contents {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
```
