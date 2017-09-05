
# Textarea

----

Textarea Input for multiline text, not for rich text entry.

## 기본 사용법

textarea 두줄이 기본 값입니다. `AtInput` 컴포넌트와 유사합니다.

:::demo
```html
<at-textarea v-model="inputValue" placeholder="Please input..."></at-textarea>
```
:::

## 미사용

textarea를 미사용상태로 만드려면 `disabled` 속성을 추가하세요

:::demo
```html
<at-textarea v-model="inputValue" placeholder="Please input..." disabled></at-textarea>
```
:::

## 문자열에 따라 변경하는 높이 (제한적)

문자열의 행에 따라 영역의 높이를 자동으로 조정합니다. 최소 및 최대 행은 `minRows`와 `maxRows`로 설정할 수 있습니다.

:::demo
```html
<p class="demo-desc">minRows=2, maxRows=4</p>
<at-textarea v-model="inputValue2" min-rows="2" max-rows="4" placeholder="Please input multiline text..."></at-textarea>
```
:::

## 문자열에 따라 변경하는 높이 (무제한)

제한 없이 자동으로 텍스트 영역의 높이를 조정하려면 `autosize` 속성을 사용하세요.

:::demo
```html
<at-textarea v-model="inputValue3" autosize placeholder="Please input multiline text..."></at-textarea>
```
:::

## Textarea 속성

| 속성      | 설명          | 타입      | 사용 가능한 값                           | 기본값  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| name | 네이티브 name과 같음 | String | - | - |
| value | textarea의 값. v-model로 양방향 바인딩을 사용 | String | - | - |
| autosize | 문자열에 따라 높이 조절 | Boolean | - | false |
| placeholder | 플레이스홀더 | String | - | - |
| disabled | textarea의 미사용 여부 | Boolean | - | false |
| autofocus | 네이티브 autofocus와 같음 | Boolean | - | false |

<script>
export default {
  data() {
    return {
      inputValue: '',
      inputValue2: '',
      inputValue3: ''
    }
  }
}
</script>

<style lang="scss" scoped>
  .at-textarea {
    & + .at-textarea {
      margin-top: 15px;
    }
  }
</style>
