# 미디어 쿼리 사용하기

* [데모](https://ovdncids.github.io/html-css-curriculum/media-query)

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Gugi&display=swap" rel="stylesheet">
    <link href="./index.css" rel="stylesheet">
    <title>미디어 쿼리</title>
  </head>
  <body>
    <div class="container">
      <ul>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
        <li>아이템</li>
      </ul>
    </div>
  </body>
</html>
```

```css
body, ul {
  margin: 0;
  padding: 0;
  font-family: 'Gugi', cursive;
}

.container {
 margin: 0 auto;
 width: 1200px;
 color: #4285F4;
}

ul {
  font-size: 0;
}

li {
  display: inline-block;
  width: 300px;
  height: 160px;
  box-sizing: border-box;
  border: 1px #DADCE0 solid;
  background-color: #F2F2F2;
  font-size: 16px;
}

@media screen and (max-width: 1200px) {
  .container {
    width: 900px;
    color: #EA4335;
  }
}

@media screen and (max-width: 900px) {
  .container {
    width: 600px;
    color: #FBBC05;
  }
}

@media screen and (max-width: 600px) {
  .container {
    width: 300px;
    color: #34A853;
  }
}
```
