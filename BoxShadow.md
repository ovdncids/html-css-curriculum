# Box shadow 속성

* [데모](https://ovdncids.github.io/html-css-curriculum/box-shadow)

```css
box-shadow: 1px 1px 1px 1px #4285F4;
```
* `box-shadow` 첫번째 값은 `x` 축을 뜻한다. (필수값)
* `box-shadow` 두번째 값은 `y` 축을 뜻한다. (필수값)
* `box-shadow` 세번째 값은 `z` 축을 뜻한다.
* `box-shadow` 네번째 값은 아이템 크기 보다 얼마나 더 큰지를 뜻한다.
* `box-shadow` 다섯번째 값은 색상을 뜻한다.
* ❔ `x`, `y`, `z`, `크기`, `색` 변경
* 그림자가 2개일 경우 설명
* `inset` 설명 (설정 빼보기)

## 활용
* `nav` 부분과 `content` 부분을 `border`로 나누지면 `width`를 계산할때 신경 쓰인다.
* 이럴때 `box-shadow` `inset`을 사용하면 효과적이다.

## 참조
https://developer.mozilla.org/ko/docs/Web/CSS/box-shadow
