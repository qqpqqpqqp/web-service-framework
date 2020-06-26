## 起動方法

```bash
# install dependencies
$ yarn install

# DEV環境のファイルを利用する場合
$ yarn run dev

#STG環境のファイルを利用する場合
#$ yarn run stg
```



## 不足パッケージのインストール

```sh
$ yarn add {$パッケージ名}
```

### Sassの環境構築

```sh
$ yarn add sass-loader node-sass
```

### pugの環境構築

```sh
$ yarn add -D pug pug-loader
```

### html圧縮の環境構築

```sh
$  yarn add @nuxtjs/html-minifier
```
nuxt.config.js
```sh
{
  modules: [
    ['@nuxtjs/html-minifier', { log: 'once', logHtml: true }]
 ]
}
```





### GraphQLの環境構築

```sh
$ yarn add @nuxtjs/apollo
$ yarn add core-js@latest2.6.2
```
