
# 폼

----

## 기본 사용

다음은 간단한 로그인 폼입니다

:::demo

```html
<at-form :model="formLogin" :rules="ruleLogin" ref="formLogin">
  <at-form-item prop="username">
    <at-input v-model="formLogin.username" placeholder="用户名">
      <template slot="prepend">
        <i class="icon icon-link"></i>
      </template>
    </at-input>
  </at-form-item>
  <at-form-item prop="password">
    <at-input v-model="formLogin.password" placeholder="密码">
      <template slot="prepend">
        <i class="icon icon-link"></i>
      </template>
    </at-input>
  </at-form-item>
  <at-form-item>
    <at-button type="primary" size="small" @click.prevent="handleSubmit('formLogin')">登录</at-button>
  </at-form-item>
</at-form>
```

:::

## 다중 폼 컨트롤

## 폼 레이아웃

레이아웃은 세가지 형식이 있습니다. `formLayout`을 설정하여 레이블 레이아웃 형태를 바꿀 수 있습니다.

## 폼 검증

## 사용자 정의 폼 검증

## 팝업에서 새 폼 사용하기

## 동적 폼 제어

<script>
  export default {
    data () {
      return {
        formLogin: {
          username: '',
          password: ''
        },
        ruleLogin: {
          username: [{
            required: true,
            message: '请输入用户名',
            trigger: 'blur'
          }],
          password: [{
            required: true,
            message: '请输入密码',
            trigger: 'blur'
          }, {
            type: 'string',
            min: 6,
            message: '密码长度不能小于6',
            trigger: 'blur'
          }]
        }
      }
    },
    methods: {
      handleSubmit (name) {
        this.$refs[name].validate(valid => {
          if (valid) {
            this.$notify({
              type: 'success',
              message: '提交成功'
            })
          } else {
            this.$notify({
              type: 'error',
              message: '校验失败'
            })
          }
        })
      }
    }
  }
</script>

<style lang="scss" scoped>
.at-input {
  width: 200px;
}
</style>
