# 설치

----

## NPM

개발할 때 `npm`을 사용해 `node` 생태계의 `webpack` 등의 툴을 사용하는 것이 좋습니다. `npm`을 이용해 패키지를 설치하면 `import` 또는 `require`를 이용해 쉽게 참조할 수 있습니다.

```bash
npm install at-ui

npm install at-ui-style
```

## CDN

`<script>`와 `<link>`를 사용하는 기존 방법으로 사용할 수도 있습니다.

 UNPKG](https://unpkg.com/at-ui/)에서 `AT-UI`의 최신 버전을 찾으세요.

```html
<!-- import Vue -->
<script src="//vuejs.org/js/vue.min.js"></script>
<!-- import CSS -->
<link rel="stylesheet" href="//unpkg.com/at-ui-style/css/at.min.css">
<!-- import JavaScript -->
<script src="//unpkg.com/at-ui/dist/at.min.js"></script>
```

#### 데모:

스크립트 태그를 사용해 리소스를 가져오면 `AT-UI`로 데모 페이지를 빠르게 만들 수 있습니다. 아래 코드를 복사하거나 [온라인 데모](https://jsbin.com/dezafos/edit?html,output)를 직접 볼 수 있습니다.

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>AT-UI Example</title>
  <link rel="stylesheet" href="//unpkg.com/at-ui-style/css/at.min.css">
  <script src="//vuejs.org/js/vue.min.js"></script>
  <script src="//unpkg.com/at-ui/dist/at.min.js"></script>
  <style>
    #app {
      display: flex;
      height: 100%;
      justify-content: center;
      align-items: center;
    }
  </style>
</head>
<body>
  <div id="app">
    <at-button @click="showMessage">Show message</at-button>
  </div>

  <script>
    new Vue({
      el: '#app',
      methods: {
        showMessage: function () {
          this.$Message('Thanks for using AT-UI')
        }
      }
    })
  </script>
</body>
</html>
```
