
# 퀵스타트

----

## 시작하기 전에

> AT-UI를 사용하기 전에, `Vue`와 `ES2015`를 먼저 익혀야합니다. 그리고 [Node.js](https://nodejs.org/en/) (≥ v6.x)가 올바르게 설치되었는지 확인하세요.

`AT-UI`는 `Vue.js` 2버전을 기반으로 합니다. 아래의 기본 사항을 숙지하시기 바랍니다.

- [Vue Components](https://kr.vuejs.org/v2/guide/components.html)
- [Single File Components](https://kr.vuejs.org/v2/guide/single-file-components.html)

## 스타터 킷

> `Vue.js`는 빠르게 싱글 페이지 앱을 개발하기 위한 [공식 CLI](https://github.com/vuejs/vue-cli)를 제공합니다. 최신 프론트엔드 개발에 필요한 기본적인 설정을 포함하고 있습니다. 적은 시간 안에 핫 리로드, 저장시 린트, 프로덕션 레디 빌드를 사용할 수 있게 됩니다.

제공하는 `vue cli template`를 이용해 SPA를 빠르게 만들 수 있습니다.

```shell
vue init at-ui/at-template my-project
```

`vue-cli`를 좋아하지 않으면 스타터킷 [at-webpack-boilerplate](https://github.com/at-ui/at-webpack-boilerplate)를 사용하세요.

## 기본적인 개발 흐름

프로덕션 프로젝트는 `Webpack`, `Rollup` 또는 `Gulp`를 사용합니다. 대부분 요청에 따라 컴포넌트를 불러올 수 있습니다. 전역 사용을 위한 `<script>` 는 권장하지 않습니다.

### 전역 컴포넌트 사용

프로젝트 엔트리 파일에서 모든 컴포넌트 또는 필수 컴포넌트를 가져옵니다.

```js
import Vue from 'vue'
import AtComponents from 'at-ui'
import 'at-ui-style'    // Import CSS

// import 'at-ui-style/src/index.scss'      // Or import the unbuilt version of SCSS

Vue.use(AtComponents)
```

모든 컴포넌트를 전역으로 가져온 경우 다음과 같이 직접 `AT-UI`의 전역 인스턴스 메소드를 사용할 수 있습니다.

```js
this.$Loading.start()
this.$Message.success(config)
this.$Modal.alert(config)
this.$Notify(config)
```

### 필요한 컴포넌트만 가져오기

로컬로 등록할 수 있는 컴포넌튼는 다른 프레임워크와 결합하는 시나리오에서 사용할 수 있습니다.

```js
import { AtInput } from 'at-ui'

export default {
  components: {
    AtInput
  },
  data () {
    return {
      value: 'O2Team'
    }
  }
}
```

템플릿에서, 사용자 정의 태그 `<at-input></at-input>`를 사용하고 `v-model`로 데이터 바인딩을 할 수 있습니다.

```html
<template>
  <div>
    <at-input v-model="value" placeholder="Please input..."></at-input>
  </div>
</template>
```

## 사용자 정의 테마

`AT-UI`의 스타일은 별도 프로젝트인 [AT-UI-Style](https://github.com/at-ui/at-ui-style)로부터 독립적입니다. 각 컴포넌트의 변수는 `at-ui-style/src/variables/default.scss`에 있습니다. 필요에 따라 컴포넌트의 스타일을 변경할 수 있습니다.
