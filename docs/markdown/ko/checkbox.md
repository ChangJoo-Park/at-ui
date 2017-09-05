
# 체크박스

----

## 기본형태

독립적인 사용을 위해 `model`을 별도로 바인딩 해야합니다.

:::demo
```html
<at-checkbox v-model="checkboxValue" label="Shenzhen">Shenzhen</at-checkbox>
<at-checkbox v-model="checkboxValue" label="Beijing">Beijing</at-checkbox>
<at-checkbox v-model="checkboxValue" label="Guangzhou">Guangzhou</at-checkbox>
```
:::

## 미사용

체크박스를 미사용 상태로 만드려면 `disabled` 속성을 `Checkbox`에 추가하세요.

:::demo
```html
<at-checkbox v-model="checkboxValue2" label="Shenzhen" disabled>Shenzhen</at-checkbox>
<at-checkbox v-model="checkboxValue3" label="O2Team" disabled checked>O2Team</at-checkbox>
```
:::

## 체크박스 그룹

배열을 사용하는 `CheckboxGroup`을 사용해 조합을 만드세요.

:::demo
```html
<at-checkbox-group v-model="checkboxValue4">
  <at-checkbox label="Shenzhen">Shenzhen</at-checkbox>
  <at-checkbox label="Beijing">Beijing</at-checkbox>
  <at-checkbox label="Shanghai">Shanghai</at-checkbox>
  <at-checkbox label="Guangzhou" disabled>Guangzhou</at-checkbox>
  <at-checkbox label="O2Team" disabled>O2Team</at-checkbox>
</at-checkbox-group>
<p class="demo-desc">{{ checkboxValue4 }}</p>
```
:::

## 전체 선택

`indeterminate` 속성은 '전체 선택'을 할 수 있도록 도와줍니다.

## Checkbox Props

| 속성      | 설명          | 타입      | 사용 가능 값                           | 기본 값  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| label | 선택 값 | String | - | - |
| disabled | 미사용 여부 | Boolean | - | false |
| checked | 체크박스가 선택된 여부 | Boolean | - | false |

## 체크박스 그룹 이벤트

| 이벤트 이름      | 설명          | 반환 값  |
|---------- |-------------- |---------- |
| checkbox-group-change | 선택된 값이 변경되면 발생합니다. | 선택된 `label`의 값 |

<script>
export default {
  data() {
    return {
      checkboxValue: ['Shenzhen'],
      checkboxValue2: [],
      checkboxValue3: ['Shenzhen'],
      checkboxValue4: ['Shenzhen', 'O2Team']
    }
  }
}
</script>
