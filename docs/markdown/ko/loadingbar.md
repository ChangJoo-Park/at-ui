
# 로딩바

----

로딩 진행을 표시하는 진행바를 전역으로 만들어 비동기 요청의 상태를 표시합니다.

재사용성을 위해 `LoadingBar`는 하나의 인스턴스만 만듭니다. `this.$Loading` 인스턴스를 직접 사용합니다.

## 기본 형태

`$Loading`으로 다음 메소드를 호출하세요: `start()`、`finish()`、`error()`

:::demo
```html
<at-button @click="start">Start</at-button>
<at-button @click="finish">Finish</at-button>
<at-button @click="error">Error</at-button>
<at-button @click="update">Update</at-button>

<script>
  export default {
    methods: {
      start () {
        this.$Loading.start()
      },
      finish () {
        this.$Loading.finish()
      },
      error () {
        this.$Loading.error()
      },
      update () {
        this.$Loading.update(50)
      }
    }
  }
</script>
```
:::

## 로딩바 메소드

| 함수 이름      | 설명          | 파라미터      |
|---------- |-------------- |---------- |
| start | 로딩을 0부터 시작. 자동으로 불러옴 | - |
| finish | 진행 완료 | - |
| error | 로딩바의 에러 타입 | - |
| update | 구체적인 진행률 | percentage |

## 로딩바 설정

`LoadingBar`에 전역 설정을 지정할 수 있습니다. 아래의 메소드를 이용합니다.

```js
this.$Loading.config({
  width: 4
})
```

:::demo
```html
<at-button @click="setWidth">{{ btnText }}</at-button>
```
:::

## 로딩바 속성

| 속성      | 설명          | 타입      | 사용 가능한 값                           | 기본값  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| width | 라인의 길이 | Number | - | 2 |

<script>
export default {
  data () {
    return {
      isSetWidth: false,
      btnText: 'Set line width to 4px'
    }
  },
  methods: {
    start () {
      this.$Loading.start()
    },
    finish () {
      this.$Loading.finish()
    },
    error () {
      this.$Loading.error()
    },
    update () {
      this.$Loading.update(50)
    },
    setWidth () {
      if (this.isSetWidth) {
        this.isSetWidth = false
        this.btnText = 'Set line width to 4px'
        this.$Loading.config({
          width: 2
        })
      } else {
        this.isSetWidth = true
        this.btnText = 'Cancel the line width to 4px'
        this.$Loading.config({
          width: 4
        })
      }
    }
  }
}
</script>
