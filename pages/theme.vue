<template lang="pug">
  #app
    Navigation
    main.l-contents(ref="width")
      .l-wrap
        h1.c-contentsHL Theme
        .c-contentsHL__lead
          p サイト設定ファイルにて設定する
          pre.c-card.p20
            code ~/assets/scss/variable/_theme.scss
        section.l-section
          h2.c-contentsHL Theme / Color
          section.l-section
            h3.c-contentsHL 基本色
            p.l-container テーマカラー、文字色、背景色の設定
            .l-container
              .p-table
                dl.l-column
                  dt.l-column__column_two テーマカラー
                  dd.l-column__column_two.bg_theme $colorTheme
                dl.l-column
                  dt.l-column__column_two 背景色
                  dd.l-column__column_two.bg_base $colorBase
                dl.l-column
                  dt.l-column__column_two 文字色
                  dd.l-column__column_two.bg_main $colorMain
                dl.l-column
                  dt.l-column__column_two サブ背景色
                  dd.l-column__column_two.bg_subBase $subColorBase
                dl.l-column
                  dt.l-column__column_two ドロワーの背景色
                  dd.l-column__column_two.bg_drawer $drawerBg
                dl.l-column
                  dt.l-column__column_two ヘッダーの背景色
                  dd.l-column__column_two.bg_header $headerBg
                dl.l-column
                  dt.l-column__column_two ボーダーカラー
                  dd.l-column__column_two.bg_border $borderColor
                dl.l-column
                  dt.l-column__column_two テキストフィールドの背景色
                  dd.l-column__column_two.bg_textField $textFieldBg
        section.l-section
          h2.c-contentsHL Theme / Width
          section.l-section
            h3.c-contentsHL 基本
            .l-container
              .p-table
                dl.l-column
                  dt.l-column__column_two 表示最大幅
                  dd.l-column__column_two {{width}}
                dl.l-column
                  dt.l-column__column_two ドロワーの幅
                  dd.l-column__column_two {{drawrWidth}}
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
