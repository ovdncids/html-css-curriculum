# 가운데 정렬이면서 위치 고정

index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="./index.css">
  <title>Document</title>
</head>
<body>
  <div class="parent">
    <div class="a">
      <div class="a1"></div>
      <div class="a2"></div>
    </div>
    <div class="b"></div>
    <div class="c">
      <div class="c2"></div>
      <div class="c1"></div>
    </div>
  </div>
</body>
</html>
```

index.css
```css
html, body, .parent {
  margin: 0;
  height: 100%;
}
.parent {
  display: flex;
  justify-content: center;
}

.a {
  position: relative;
}

.a1 {
  position: fixed;
  background-image: linear-gradient(to bottom, red, yellow);
  width: 200px;
  height: 100%;
}
.a2 {
  background-color: black;
  width: 200px;
  height: 1600px;
}

.b {
  background-image: linear-gradient(to bottom, green, blue);
  min-width: 200px;
  height: 100%;
}

.c {
  position: relative;
}

.c1 {
  position: fixed;
  background-image: linear-gradient(to bottom, black, white);
  min-width: 200px;
  height: 100%;
}

.c2 {
  background-color: orange;
  width: 200px;
  height: 200px;
}
```
