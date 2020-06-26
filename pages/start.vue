<template lang="pug">
  #app
    Navigation
    main.l-contents(ref="width")
      .l-wrap
        h1.c-contentsHL Start
        .c-contentsHL__lead 導入手順は以下の通りです。
        section.l-section
          h2.c-contentsHL 環境構築
          section.l-section
            h3.c-contentsHL jsパッケージマネージャーのインストール
            .l-container
              pre.c-card.p20
                code
                    |$ brew install yarn
          section.l-section
            h3.c-contentsHL 本プロジェクトのダウンロード
            .l-container
              a.c-regularButton.c-button_disabled ダウンロード
          section.l-section
            h3.c-contentsHL セットアップ
            .l-container readme.md を参照
          section.l-section
            h3.c-contentsHL おすすめのパッケージ(任意)
            ul.c-lists.l-container
              li.c-lists__text.l-column.l-column_nowrap
                  .w200
                    a(href="https://qiita.com/takanorip/items/d1e8618800d951780f4b" target="_blank" rel="noopener") apollo
                  .l-column__column_grow GraphQL使うなら
              li.c-lists__text.l-column.l-column_nowrap
                  .w200
                    a(href="https://tecb.jp/blog/996" target="_blank" rel="noopener") vue-touch
                  .l-column__column_grow ドロワーのスマホ対応したい場合
</template>
<script>
import Navigation from '~/components/Navigation.vue'
export default {
  data: function () {
    return {
      width: 0,
      drawrWidth: 0
    }
  },
  created: function(){


  },
  mounted: function(){
    this.getWidth();
    this.getDrawrWidth();
  },
  methods: {
    getWidth: function () {
      if (process.client){
        var element = this.$refs.width;
        var cssStyleDeclaration = getComputedStyle( element, null ) ;
        this.width = cssStyleDeclaration.getPropertyValue( "max-width" ) ;
      }
    },
    getDrawrWidth: function () {
      if (process.client){
        var element = this.$refs.width;
        var cssStyleDeclaration = getComputedStyle( element, null ) ;
        this.drawrWidth = cssStyleDeclaration.getPropertyValue( "padding-left" ) ;
      }
    },
  },
  components: {
    Navigation
  }
}




</script>

<style lang="scss" scoped>
// ★変数一覧 ★★★★★★★★★★★★★★★★★★
@import "~/assets/scss/variable/_structure";
@import "~/assets/scss/variable/_theme";

.bg{
  &_theme{
    background-color: $colorTheme;
  }
  &_base{
    background-color: $colorBase;
  }
  &_main{
    background-color: $colorMain;
    color: $colorBase;
  }
  &_subBase{
    background-color: $subColorBase;
  }
  &_drawer{
    background-color: $drawerBg;
  }
  &_header{
    background-color: $headerBg;
  }
  &_border{
    background-color: $borderColor;
  }
  &_textField{
    background-color: $textFieldBg;
  }
}

</style>
