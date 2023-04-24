# 모듈

## 고전적인 방식

```html
<!-- 중략 -->
<script src="main.js"></script>
<script src="common.js"></script>
<script src="library1.js"></script>
<script src="library2.js"></script>
```

```js
/* main.js */
window.onload = function () {
  /**
   * 1. common에 대한 의존성을 명확하게 확인할 수 없음
   * 2. 전역 모듈에 대한 네임스페이스 오염 (많은 라이브러리)
   * 3. 재사용성 및 가독성을 위해
   */

  common.init(); // common.js에 정의된 변수 호출
};
```

---

## `NodeJs` 모듈 시스템

기본적으로 `commonjs` 방식을 따르고있다.

```js
const _ = require("lodash"); // 가져오기

module.export = {
  // 내보내기
  add: function Add(a, b) {
    return a + b;
  },
};
```

## ES6 표준 모듈 시스템(ESM)

`Webpack`, `TypeScript`, `Browser` 등

기본적으로 ES6 모듈 방식을 사용합니다.

```js
import _ from "lodash"; //가져오기

// 내보내기
export function Add(a, b) {
  return a + b;
}

export default Add;
```

이 두가지 방식 모두 기본적으로 전역 스코프가 아닌 **별도의 로컬한 스코프**를 가지게됩니다.

---
