<p align="center">
  <a href="https://at.aotu.io/">
    <img width="200" src="http://storage.360buyimg.com/mtd/home/logo-at1502718221686.svg">
  </a>
</p>

# AT UI

[![NPM][npm-version-image]][npm-version-url] [![david-dm][david-dm-image]][david-dm-url] [![travis][travis-image]][travis-url]

AT-UI는 모듈 방식의 빠르고 강력한 웹 인터페이스를 위한 프론트엔드 UI 프레임워크입니다.

[中文 README](README.zh-CN.md)
[한국어 README](README.ko-KR.md)

## 기능

- `Vue`를 기반으로 함
- npm + webpack + babel 프론트엔드 개발 방식을 따름
- ES2015 지원
- CSS 스타일에 독립적이며, 일관된 유저 인터페이스를 만들 수 있습니다. (참고: [AT-UI-Style](https://github.com/at-ui/at-ui-style))
- 사용자 친화적인 API

## 지원 환경

- 최신 브라우저와 인터넷 익스프롤러 9 이상
- [Electron](http://electron.atom.io/)

## 설치

- `npm`을 추천합니다.

```bash
npm install at-ui
```

- 또는 전역 사용을 위해 `<script>`를 사용합니다.

```html
<script type="text/javascript" src="at.min.js"></script>
```

## 사용방법

`AT-UI`의 스타일은 독립적이기 때문에 분리된 프로젝트로 존재합니다. 그러므로 `AT-UI`를 사용하기 이전에 `AT-UI-Style`을 설치 해야 합니다. npm 또는 script 태그를 사용하세요.

```bash
npm install at-ui-style
```

or

```html
<link rel="stylesheet" href="at.min.css" />
```

## 기여하기

버그를 발견하거나 풀 리퀘스트 또는 문서를 개선하는 등의 어떠한 기여도 좋습니다. 기여를 시작하려면 [contribution guidelines](https://github.com/at-ui/at-ui/blob/master/.github/CONTRIBUTING.md)를 읽어보세요. 고맙습니다!

## 라이센스

MIT

[npm-version-image]: https://img.shields.io/npm/v/at-ui.svg?style=flat-square
[npm-version-url]: https://www.npmjs.com/package/at-ui
[david-dm-image]: https://david-dm.org/AT-UI/at-ui.svg?style=flat-square
[david-dm-url]: https://david-dm.org/AT-UI/at-ui
[travis-image]: https://img.shields.io/travis/AT-UI/at-ui/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/AT-UI/at-ui
