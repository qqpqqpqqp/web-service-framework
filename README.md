# web-service-framework

WEBプロダクトを作成する際のJS/CSSフレームワークです。基礎的なUIコンポーネントが用意されており、より簡易的にスタート出来ます。

## 起動方法

```bash
# install dependencies
$ yarn install
or
$ npm install

# DEV環境のファイルを利用する場合
$ yarn run dev
or
$ npm run dev

#STG環境のファイルを利用する場合
#$ yarn run stg
```



## 不足パッケージのインストール

```sh
$ yarn add {$パッケージ名}
or
$ npm install {$パッケージ名} 
```

### Sassの環境構築

```sh
$ yarn add sass-loader node-sass
or
$ npm install sass-loader node-sass
```

### pugの環境構築

```sh
$ yarn add -D pug pug-loader
or
$ npm install pug pug-loader
```

### html圧縮の環境構築

```sh
$ yarn add @nuxtjs/html-minifier
or
$ npm install @nuxtjs/html-minifier
```


## 不足パッケージのインストール(オプション)

### GraphQLの環境構築

```sh
$ yarn add @nuxtjs/apollo
$ yarn add core-js@latest2.6.2
```
