# vue3-paru

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```


## setting

1. [Chrome](https://www.google.com/intl/ko_kr/chrome/)
2. [Visual studio code](https://code.visualstudio.com/download)
3. [Node.js](https://nodejs.org/ko/download)
4. [Vue.js Devtools](https://chrome.google.com/webstore/search/vue.js%20devtools)
5. [Vue Language Features (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.volar)

[Vue.js 3 한글 가이드](https://v3-docs.vuejs-korea.org/guide/quick-start.html#creating-a-vue-application): 시작 방법, 예제 코드, Demo까지 실습해 볼 수 있다.

[Vue.js + ES6](https://joshua1988.github.io/es6-online-book/): vue 개발할 때, 많이 사용하는 es6 문법

[Cracking Vue.js](https://joshua1988.github.io/vue-camp/): vue 개발 팁

[Vue Router](https://v3.router.vuejs.org/kr/): vue router 핸드북

[Vuex](https://vuex.vuejs.org/): vuex 핸드북

[Pinia](https://pinia.vuejs.kr/): vuex5 버전과 거의 같은 상태관리 라이브러리 Pinia 사이트

[Vue CLI](https://cli.vuejs.org/): vue cli 핸드북

[타입스크립트 핸드북](https://joshua1988.github.io/ts/)

[웹팩 핸드북](https://joshua1988.github.io/webpack-guide/)

[Vue 테스팅 핸드북](https://lmiller1990.github.io/vue-testing-handbook/ko/)

### vue3 create with vite

```sh
npm init vue@latest
```

vue + vite 생성

### vue3 create with webpack

```sh
vue create '프로젝트 명'
```

vue + webpack 생성

## 개발에 도움 되는 설정

### jsconfig.json 생성

```sh
{
  "compilerOptions": {
    "baseUrl": "./",
    "paths": {
      "~/*": [
        "*"
      ],
      "@/*": [
        "src/*"
      ]
    },
  },
  "exclude": [
    "node_modules",
    "dist"
  ]
}
```

"paths" - 개발할 때, @/ 입력시 ./src/* 경로를 빠르게 찾아주는 설정

### .eslintrc.cjs

```sh
module.exports = {
rules: {
    'no-console': 'off',
    // 'no-console': process.env.NODE_ENV === 'production' ? 'warn' : 'off',
    // 'no-debugger': process.env.NODE_ENV === 'production' ? 'warn' : 'off',
    'prettier/prettier': [
      'error',
      {
        singleQuote: true,
        semi: true,
        useTabs: false,
        tabWidth: 2,
        trailingComma: 'all',
        printWidth: 80,
        bracketSpacing: true,
        arrowParens: 'avoid',
      },
    ],
  },
}
```

#### eslint 

ESLint는 자바스크립트 코드에서 발견되는 문제시되는 패턴들을 식별하기 위한 정적 코드 분석 도구이다. 

#### prettier

소스코드를 설정에 따라 자동으로 꾸며준다.

### scss

```sh
npm i -D scss
```

css를 더 직관적인 문법으로 작성할 수 있게 도와준다.

## build

### package.json

```sh
"scripts": {
    "dev": "vite",
    "build": "vite build --watch",
    "preview": "vite preview",
    "lint": "eslint . --ext .vue,.js,.jsx,.cjs,.mjs --fix --ignore-path .gitignore",
    "format": "prettier --write src/"
  },
  
  
  "dependencies": {
    "pinia": "^2.0.32",
    "vue": "^3.2.47",
    "vue-router": "^4.1.6"
  },
  "devDependencies": {
    "@rushstack/eslint-patch": "^1.2.0",
    "@vitejs/plugin-vue": "^4.0.0",
    "@vitejs/plugin-vue-jsx": "^3.0.0",
    "@vue/eslint-config-prettier": "^7.1.0",
    "eslint": "^8.34.0",
    "eslint-plugin-vue": "^9.9.0",
    "prettier": "^2.8.4",
    "vite": "^4.1.4"
  }
```

#### --watch

파일 변경 시 자동 빌드

#### "dependencies"

빌드에 포함되는 의존 라이브러리

#### "devDependencies"

빌드에 포함되지 않는 라이브러리, 빌드와 개발에 도움을 주는 의존 라이브러리

### vite.config.js

```sh
import { fileURLToPath, URL } from 'node:url';

import { defineConfig } from 'vite';
import vue from '@vitejs/plugin-vue';
import vueJsx from '@vitejs/plugin-vue-jsx';

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [vue(), vueJsx()],
  resolve: {
    alias: {
      '@': fileURLToPath(new URL('./src', import.meta.url)),
    },
  },
  build: {
    outDir: '../src/main/resources/static',
  },
  server: {
    proxy: {
      '/api': 'http://localhost:8080',
    },
  },
});
```

### build 명령어

```sh
npm run build
```

outDir에 입력된 경로에 빌드한다.

### local dev 

```sh
npm run dev
```

### server.proxy
cors 해결하는 방법 중 하나.


asdsadadas
