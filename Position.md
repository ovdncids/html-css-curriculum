# Position 속성

* [데모](https://ovdncids.github.io/html-css-curriculum/position)

## z-index
* z축(높이)에서 위로 보여줄 순위를 정한다.
* 모든 엘리먼트의 기본 z-index 값은 0이다.
* 동일한 z-index 값일 경우 아래에 있는 앨리먼트가 위로 보여지게 된다.

## 오프셋(offset)
* top, right, bottom, left를 사용해 이동한 거리를 말한다.

<!-- 구글 색상
파란색: #4285F4
빨간색: #EA4335
노란색: #FBBC05
녹색: #34A853

#235bb6 -->

## static
```css
position: static;
```
* 기본 속성으로 position을 지정하지 않으면 `position: static;`이 된다.
* 문서 안에서 자신의 영역을 유지한다.
* `top, right, bottom, left, z-index` 값이 수정은 되지만 적용이 되지 않는다.
* ❔ `.static` class에 `top: 50px;` `left: 50px;` `z-index: 100;` 적용

## relative
```css
position: relative;
```
* static과 같이 문서 안에서 자신의 영역을 유지한다.
* `top, right, bottom, left` 위치를 변경 하면, 자신의 영역은 그대로지만 해당 위치에만 떠 있게 된다.
* ❔ `.relative` class에 `top: 50px;` `left: 50px;` 적용
* ❔ `position: relative;` 활성화, 비활성화 하기
* `z-index: 0;` 보다 작지 않으면 항상 `position: static;` 보다 위에 보이게 된다
* ❔ `z-index: -1;` 적용
* ❔ `top: 150px;` 적용
* ❔ `z-index: 0;` 적용, `z-index: 1;` 적용
* ❔ `top: 250px;` 적용
* ❔ `z-index: 0;` 적용
* ❔ `top: 0; left: 100px;` 적용

## absolute
```css
position: absolute;
```
* 문서 안에서 자신만에 영역을 유지 하지 않는다. 따라서 항상 떠 있다.
* 기본 위치는 자신의 바로 위에 엘리먼트 다음에 위치 한다.
* 조상이 모두 `position: static;`일 경우: `top, right, bottom, left` 위치는 문서 최상단이 된다.
* ❔ `.absolute` class에 `top: 50px;` `left: 50px;` 적용
* ❔ `top: 150px;` 적용
* ❔ `z-index: -1;` 적용
* ❔ `z-index: 1;` 적용
* 조상이 `position: static;`이 아닐 경우: 해당 조상 기준으로 `top, right, bottom, left` 위치가 결정 된다.
* ❔ `.parent` class에 `position: relative;` 적용
* ❔ `.parent` class에 `position: absolute;` 적용

## fixed
```css
position: fixed;
```
* 기본 위치는 자신의 바로 위에 엘리먼트 다음에 위치 한다.
* absolute와 비슷하지만 차이점은 조상과 상관 없이 `top, right, bottom, left` 위치는 문서 최상단이 된다.
* ❔ `.fixed` class에 `top: 50px;` `left: 50px;` 적용
* ❔ `z-index: 0;` 적용
* ❔ `top: 150px;` 적용
* ❔ `z-index: 1;` 적용
* ❔ `.parent` class에 `position: fixed;` 적용
* ❔ `.parent` class에 `position` 비활성화

## sticky
* IE에서 작동 안함

## 참조
https://developer.mozilla.org/ko/docs/Web/CSS/position

https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Positioning/Understanding_z_index/Adding_z-index
