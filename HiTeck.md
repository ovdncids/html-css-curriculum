# 고급 기능

## Anchor 이동 할때 해더 영역 밑으로 이동
```html
<header>해더</header>
<h1 id="h1-tag" style="position: relative; margin-top: -76px; height: 76px; visibility: hidden; z-index: -1"></div>
<div>내용</div>
<a href="#h1-tag">이동</a>
```

## Mac에서 스크롤 항상 보이기
https://stackoverflow.com/questions/7492062/css-overflow-scroll-always-show-vertical-scroll-bar
```css
::-webkit-scrollbar {
  -webkit-appearance: none;
  width: 7px;
}

::-webkit-scrollbar-thumb {
  border-radius: 4px;
  background-color: rgba(0, 0, 0, .5);
  box-shadow: 0 0 1px rgba(255, 255, 255, .5);
}
```
