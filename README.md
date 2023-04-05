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

[Vue.js 3 한글 가이드](https://v3-docs.vuejs-korea.org/guide/quick-start.html#creating-a-vue-application)

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

### scss
```sh
npm i -D scss
```
