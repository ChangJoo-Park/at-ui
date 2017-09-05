
# 페이지 매김

----

긴 리스트는 페이지 매김으로 여러 페이지로 나눌 수 있으며 한번에 한 페이지만 불러옵니다.

## 기본 형태

8페이지 미만.

:::demo
```html
<at-pagination :total="60"></at-pagination>
```
:::

## 더 많은 페이지

8 페이지 이상.

:::demo
```html
<at-pagination :total="100"></at-pagination>
```
:::

## 전체 갯수 출력

데이터의 양을 표시하려면 `show-total` 속성을 추가하세요

:::demo
```html
<at-pagination :total="80" show-total></at-pagination>
```
:::

## Quick Jumper

quick-jump 버튼을 보려주기 위해 `show-quickjump` 속성을 추가하세요

:::demo
```html
<at-pagination :total="100" show-quickjump></at-pagination>
```
:::

## 각 페이지의 항목 갯수 설정

각 페이지에 표시될 항목 수를 설정할 수 있습니다.

:::demo
```html
<at-pagination :total="100" show-sizer></at-pagination>
```
:::

## 전체 기능 사용

페이지 매김의 전체 기능을 사용합니다.

:::demo
```html
<at-pagination :total="100" show-total show-sizer show-quickjump></at-pagination>
```
:::

## 미니 페이지 매김

작은 크기의 페이지매김을 사용하려면 `size` 속성을 `small`로 설정하세요.

:::demo
```html
<at-pagination size="small" :total="100" show-total show-sizer show-quickjump></at-pagination>
```
:::

## 심플 모드

`simple` 속성을 설정하면 심플 모드로 출력됩니다.

:::demo
```html
<at-pagination :total="100" simple></at-pagination>
<at-pagination :total="100" size="small" simple></at-pagination>
```
:::

## 페이지매김 속성

| 속성      | 설명          | 타입      | 사용 가능한 값                           | 기본값  |
|---------- |-------------- |---------- |-----------------------------  |-------- |
| current | current page number | Number | - | 1 |
| total | total number of data | Number | - | 0 |
| page-size | amount shown in each page | Number | - | 10 |
| page-size-opts | The configuration of switching the amount of data shown in each page | Array | - | [10, 20, 30, 40] |
| show-total | to display the total number and range | Boolean | - | false |
| show-sizer | determine whether `page-size` can be changed | Boolean | - | false |
| show-quickjump | determine whether you can jump to a page directly | Boolean | - | false |
| size | specify the size of Pagination | String | `small` | - |
| simple | determine whether to use simple mode | Boolean | - | false |

## Pagination Events

| 이벤트 이름      | 설명          | 반환값  |
|---------- |-------------- |---------- |
| page-change | 페이지 변경시 발생 | page number |
| pagesize-change | 페이지 크기가 변경되면 발생 | page size |

<style lang="scss" scoped>
  .at-pagination + .at-pagination {
    margin-top: 16px;
  }
</style>
