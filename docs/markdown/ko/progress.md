# 프로그레스

----

이벤트의 진행 상황 및 상태를 표시하는데 사용합니다.

## 기본형태

진행 상황이 `100%`에 도달하면 자동으로 `success`로 설정됩니다.

:::demo
```html
<at-progress :percent="0"></at-progress>
<at-progress :percent="60"></at-progress>
<at-progress :percent="100"></at-progress>
<at-progress :percent="50" status="error"></at-progress>
```
:::

## 미니 프로그레스

좁은 영역에는 미니 프로그레스를 사용해야합니다. `stroke-width` 속성으로 프로그레스의 폭을 설정하세요.

:::demo
```html
<div class="row no-gutter">
  <div class="col-sm-24 col-md-12">
    <at-progress :percent="0" :stroke-width="4"></at-progress>
    <at-progress :percent="60" :stroke-width="4"></at-progress>
    <at-progress :percent="100" :stroke-width="4"></at-progress>
    <at-progress :percent="50" status="error" :stroke-width="4"></at-progress>
  </div>
</div>
```
:::

## 동적 프로그레스

진행 상황을 보려면 아래 버튼을 클릭하십시오.

:::demo
```html
<at-progress :percent="percent"></at-progress>
<at-button-group size="small">
  <at-button @click="descPercent"><i class="icon icon-minus"></i></at-button>
  <at-button @click="inscPercent"><i class="icon icon-plus"></i></at-button>
</at-button-group>

<script>
  export default {
    data () {
      return {
        percent: 0
      }
    },
    methods: {
      descPercent () {
        this.percent -= 10
        this.percent = this.percent < 0 ? 0 : this.percent
      },
      inscPercent () {
        this.percent += 10
        this.percent = this.percent > 100 ? 100 : this.percent
      }
    }
  }
</script>
```
:::

## 프로그레스 속성

| 속성      | 설명          | 타입      | 사용가능한 값                           | 기본값  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| percent | 프로그레스의 진행율 | Number | - | 0 |
| status | 프로그레스 상태 | String | `success`, `error` | - |
| stroke-width | 프로그레스 바의 길이 | Number | - | 8 |

## 프로그레스 이벤트

| 이벤트 이름      | 설명          | 반환 값  |
|------------- |-------------- |---------- |
| on-status-success | 진행률의 진행율이 `100%`가 되면 발생 | event |

<style lang="scss" scoped>
.at-progress {
  margin-bottom: 8px;
}
</style>

<script>
export default {
  data () {
    return {
      percent: 0
    }
  },
  methods: {
    descPercent () {
      this.percent -= 10
      this.percent = this.percent < 0 ? 0 : this.percent
    },
    inscPercent () {
      this.percent += 10
      this.percent = this.percent > 100 ? 100 : this.percent
    }
  }
}
</script>
