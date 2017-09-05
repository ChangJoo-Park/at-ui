
# 슬라이더

----

슬라이더는 지정된 숫자 범위 안에서 값을 제어할 때 사용합니다.

## 기본

기본 슬라이더에 `v-model` 값을 바인딩하여 사용합니다. 범위는 `0~100`이 기본입니다.

:::demo
```html
<at-slider v-model="value"></at-slider>
```
:::

## 미사용

슬라이더를 사용하지 않게 설정하려면 `disabled` 속성을 슬라이더에 추가하세요

:::demo
```html
<at-slider v-model="value2" disabled></at-slider>
```
:::

## 사용자 정의 범위

최소, 최대 값은 `min`과 `max` 속성으로 설정합니다.

:::demo
```html
<at-slider v-model="value3" :min="20" :max="80"></at-slider>
```
:::

## 이산 값

`step` 속성을 이용해 슬라이더의 간격을 조정할 수 있습니다. 값의 간격은 `1`이 기본값입니다.

:::demo
```html
<at-slider v-model="value4" :step="10"></at-slider>
```
:::

## 슬라이더 속성

| 속성      | 설명          | 타입      | 사용가능한 값                           | 기본값  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| value | slider의 값, `v-model`로 양방향 바인딩합니다. | Number | - | - |
| step | 슬라이더가 값을 단계별로 처리할 수 있는 정도 | Number | - | 1 |
| min | 최소값 | Number | - | 0 |
| max | 최대값 | Number | - | 100 |
| disabled | 슬라이더 비활성화 여부 | Boolean | - | false |

## 슬라이더 이벤트

| 이벤트      | 설명          | 반환 값  |
|---------- |-------------- |---------- |
| change | 슬라이더가 변경될 때 발생하는 이벤트 | value |

<script>
export default {
  data() {
    return {
      value: 0,
      value2: 20,
      value3: 30,
      value4: 50
    }
  }
}
</script>
