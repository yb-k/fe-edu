# CSS


# 기본 개념
Cascading Style Sheets(`CSS`)는 `HTML`이나 `XML`로 작성된 문서의 표시 방법을 기술하기 위한 **스타일 시트 언어**입니다.

`CSS`는 요소가 화면, 종이, 음성이나 다른 매체 상에 어떻게 **렌더링**되어야 하는지 지정합니다.

```css
p {
  color: 'red'
}
```

## CSS 단위

스타일에서 크기를 지정할때 사용하는 단위는 다양합니다.

크게 `상대 길이 단위`와 `절대 길위 단위` 두가지로 분류됩니다.

### 절대 길이 단위

항상 동일한 크기로 간주됩니다.

`px`, `cm`, `mm`, `in`, `pt` 등이 있습니다.


### 상대 길이 단위

상위 요소의 글꼴 크기 또는 `viewport`에 영향을 받는 단위 입니다.

비교적 많이 사용하는 4가지는 아래와 같습니다.

|단위|설명|
|--|--|
|em|요소의 글꼴 크기|
|rem|루트 요소의 글꼴 크기|
|vw|viewport 너비의 1%|
|vh|viewport 높이의 1%|

> `%`(퍼센트)는 부모 요소의 길이를 기준으로 합니다.

전체 단위는 아래의 링크를 통해 확인해보시길 바랍니다.

> [CSS 값과 단위](https://developer.mozilla.org/ko/docs/Learn/CSS/Building_blocks/Values_and_units)


## 크로스 브라우저

브라우저별로 기본 스타일은 상이 하게 구현되어있습니다.

일관성있는 스타일을 유지하기 위해서 아래의 `css`를 사용하기도 합니다.

- [Reset CSS](https://meyerweb.com/eric/tools/css/reset/)

  - 적용된 기본 스타일은 해제(초기화)합니다.

- [Normalize CSS](https://necolas.github.io/normalize.css/)

  - 기본 스타일을 활용하여 일관성있게 수정합니다.

> `Bootstrap`과 같은 CSS 프레임워크에는 이미 포함하고있다.

> `postcss autoprefixer`?

## CSS 방법론

`CSS` 설계 및 작성를 올바르게 함으로써 아래와 같은 효과를 기대해볼 수 있습니다.

- 코드의 재사용성
- 유지보수성
- 확장성
- **클래스명으로 무슨 의미인지 예측 가능하도록** (가독성)

### 작성 방법
- 적절한 의미 사용
- 중첩 선택자
- 모듈화
- 명명 규칙 (방법론)

대표적으로 아래와 같은 방법론이 있습니다.
|방법론|설명|특징
|--|--|--|
|BEM (Block Element Modifier)|컴포넌트(구조화) 설계방식|재사용성, 직관적|
|OOCSS (Object Oriented CSS)|객체지향 설계방식|DRY코드(반복X)|
|SMACSS (Scalable and Modular Architecture for CSS)|모듈화 설계방식|OOCSS + BEM (핵심 컨셉을 차용)|


### 반응형 웹개발

**미디어쿼리**

화면 크기에 따른 스타일 적용

```css
@media (min-width:320px)  { /* smartphones, portrait iPhone, portrait 480x320 phones (Android) */ }
@media (min-width:480px)  { /* smartphones, Android phones, landscape iPhone */ }
@media (min-width:600px)  { /* portrait tablets, portrait iPad, e-readers (Nook/Kindle), landscape 800x480 phones (Android) */ }
@media (min-width:801px)  { /* tablet, landscape iPad, lo-res laptops ands desktops */ }
@media (min-width:1025px) { /* big landscape tablets, laptops, and desktops */ }
@media (min-width:1281px) { /* hi-res laptops and desktops */ 
```