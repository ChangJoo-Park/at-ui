# 태그

----

## 기본 태그

태그에 닫을 있는 버튼을 만드려면 `closable` 속성을 `Tag`에 추가하세요. 버튼을 클릭했을 때 `on-close` 이벤트를 트리거합니다.

:::demo
```html
<at-tag>Tag One</at-tag>
<at-tag>Tag Two</at-tag>
<at-tag>Tag Three</at-tag>
<at-tag name="Tag Four" closable v-if="show" @on-close="handleClose">Tag Four</at-tag>
```
:::

## 색과 함께 사용하기

색상이 있는 태그를 사용할 수 있습니다. `color`를 설정하세요. `color="#6190E8"`와 같이 16진수 값을 사용할 수 있습니다.

:::demo
```html
<at-tag color="default">Tag One</at-tag>
<at-tag color="primary">Tag Two</at-tag>
<at-tag color="success">Tag Three</at-tag>
<at-tag color="error">Tag Four</at-tag>
<at-tag color="warning">Tag Five</at-tag>
<at-tag color="info">Tag Six</at-tag>
<at-tag color="#ecefce">#ecefce</at-tag>
```
:::

## 태그 속성

| 속성      | 설명          | 타입      | 사용 가능한 값                           | 기본값  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| name | close 이벤트에 사용 된 태그의 이름 | Boolean | — | false |
| color | type | String / Hex | Hex value 또는 `default`, `primary`, `success`, `error`, `warning`, `info` | default |
| closable | 닫기가 가능한지 여부 | Boolean | — | false |

## 태그 이벤트

| Event Name      | 설명          | Return Value  |
|---------- |-------------- |---------- |
| on-close | 닫힐 때 발생 | event |

<script>
  export default {
    data () {
      return {
        show: true
      }
    },
    methods: {
      handleClose (evt, name) {
        this.$Message.info(`Close Tag - ${name}`)
        this.show = false
      }
    }
  }
</script>
