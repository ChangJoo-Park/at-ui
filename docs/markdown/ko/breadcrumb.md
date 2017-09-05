
# 이동경로

----

이동경로는 계층 구조에서 현재 위치를 표시하여 상위 노드로의 탐색을 제공합니다.

## 기본 형태

`at-breadcrumb`와 `at-breadcrumb-item`을 사용해 이동경로를 만들고 `href` 속성을 가진 링크를 추가하세요.

:::demo
```html
<at-breadcrumb>
  <at-breadcrumb-item>Home</at-breadcrumb-item>
  <at-breadcrumb-item href="#/en/docs/introduction">Components</at-breadcrumb-item>
  <at-breadcrumb-item>Breadcrumb</at-breadcrumb-item>
</at-breadcrumb>
```
:::

## Vue Router와의 통합

`vue-router`와 사용할 수 있습니다. `object`를 `to` 속성에 전달하면 됩니다. 새 히스토리가 필요하지 않으면 `Breadcrumb Item`에 `replace` 속성을 추가하세요.

:::demo
```html
<at-breadcrumb>
  <at-breadcrumb-item>Home</at-breadcrumb-item>
  <at-breadcrumb-item :to="{ name: 'Layout-en' }">Layout</at-breadcrumb-item>
  <at-breadcrumb-item :to="{ name: 'Color-en' }" replace>Color</at-breadcrumb-item>
  <at-breadcrumb-item>Breadcrumb</at-breadcrumb-item>
</at-breadcrumb>
```
:::

## 구분자 설정

구분자는 `seperator` 속성으로 설정할 수 있습니다. `HTML String`을 지원합니다.

:::demo
```html
<at-breadcrumb separator=">">
  <at-breadcrumb-item>Home</at-breadcrumb-item>
  <at-breadcrumb-item href="#/en/docs/introduction">Components</at-breadcrumb-item>
  <at-breadcrumb-item>Breadcrumb</at-breadcrumb-item>
</at-breadcrumb>
```
:::


## Breadcrumb 속성

| 속성      | 설명          | 타입      | 사용 가능한 값                          | 기본값  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| separator | 사용자 정의 구분자 | String | - | `/` |

## BreadcrumbItem 속성

| 속성      | 설명          | 타입      | 사용 가능한 값                          | 기본값  |
|---------- |-------------- |---------- |--------------------------------  |-------- |
| href | `<a>` 태그의 `href` 속성과 같음 | String | - | - |
| to | `vue-router` 객체, `vue-router`의 `to` 속성과 같음 | String / Object | - | - |
| replace | `to`로 새 히스토리를 만들지 여부 설정  | Boolean | - | false |
