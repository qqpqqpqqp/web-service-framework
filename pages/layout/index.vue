<template lang="pug">
  #app
    Navigation
    main.l-contents(:class='{view : contents}')
      Tag(:box="'.l-contents'" v-if="contents")
      .l-wrap(:class='{view : wrap}')
        Tag(:box="'.l-wrap'" v-if="wrap")
        h1.c-contentsHL Layout
        .c-contentsHL__lead
          p ブロックレイアウト用。余白のリズムを均一化出来る。
      section.l-section(:class='{view : section}')
        Tag(:box="'h2.l-section'" v-if="section")
        .l-wrap.l-container(:class='{view : wrap}')
          Tag(:box="'.l-wrap'" v-if="wrap")
          h2.c-contentsHL  Layout / Contents
          .l-container ページ内コンテンツ用の最上位要素。表示エリア横いっぱいに要素を配置可能。※Navigationは抜いても.l-contentsは機能します。
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            input#boxContents(type="checkbox" value="contents" v-model="contents")
            label(for="boxContents") .l-contentsを可視化
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            pre.c-card.p20
              code
                  |#app
                  |    Navigation
                  |    main.l-contents
        img.fullImg(src="~/assets/images/panorama.jpg")
      .l-wrap(:class='{view : wrap}')
        Tag(:box="'.l-wrap'" v-if="wrap")
        section.l-section(:class='{view : section}')
          Tag(:box="'h2.l-section'" v-if="section")
          h2.c-contentsHL Layout / Wrap
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            p 左右の内側余白を持ち、付与したい要素全体を囲って使う。
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            input#boxWrap.mr6(type="checkbox" value="wrap" v-model="wrap")
            label(for="boxWrap") .l-wrap を可視化
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            pre.c-card.p20
              code
                  |.l-wrap
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            img.fullImg(src="~/assets/images/panorama.jpg")
        section.l-section(:class='{view : section}')
          Tag(:box="'h2.l-section'" v-if="section")
          h2.c-contentsHL Layout / Section
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            p hタグ(h2/h3)を内包する。外側下部余白を持つ。
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            input#boxSection.mr6(type="checkbox" value="section" v-model="section")
            label(for="boxSection") .l-section を可視化
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            pre.c-card.p20
              code
                  |section.l-section
                  |    h2.c-contentsHL 見出し
          section.l-section(:class='{view : section}',v-for="n in 2")
            Tag(:box="'h3.l-section'" v-if="section")
            h3.c-contentsHL 見出し3
            .l-container(:class='{view : container}')
              Tag(:box="'.l-container'" v-if="container")
              p 内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
        section.l-section(:class='{view : section}')
          Tag(:box="'h2.l-section'" v-if="section")
          h2.c-contentsHL Layout / Container
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            p 下側の外側余白を持ち、小さめのグループ単位で使う。
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            input#boxContainer.mr6(type="checkbox" value="container" v-model="container")
            label(for="boxContainer") .l-container を可視化
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            pre.c-card.p20
              code
                  |.l-container
          section.l-section(:class='{view : section}',v-for="n in 2")
            Tag(:box="'h3.l-section'" v-if="section")
            h3.c-contentsHL 見出し3
            .l-container(:class='{view : container}')
              Tag(:box="'.l-container'" v-if="container")
              p 内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
        section.l-section(:class='{view : section}')
          Tag(:box="'h2.l-section'" v-if="section")
          h2.c-contentsHL Layout / scrollX
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            p 可変不可要素のレスポンシブ対応用。内包する要素がウィンドウの幅を超えたとき、横スクロールする。
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            input#boxscrollX.mr6(type="checkbox" value="scrollX" v-model="scrollX")
            label(for="boxscrollX") .l-scrollX を可視化
          .l-container(:class='{view : container}')
            Tag(:box="'.l-container'" v-if="container")
            pre.c-card.p20
              code
                  |.l-scrollX
          section.l-section(:class='{view : section}')
            Tag(:box="'h3.l-section'" v-if="section")
            h3.c-contentsHL 見出し3
            .l-scrollX(:class='{view : scrollX}')
              table.p-table
                Tag(:box="'.l-scrollX'" v-if="scrollX")
                tr
                  th(v-for="n in 12") X列
                tr(v-for="n in 3")
                  td(v-for="n in 12") X行
</template>

<script>
import Navigation from '~/components/Navigation.vue'
import Tag from '~/components/layout/Tag.vue'
export default {
  data: function () {
    return {
      contents:false,
      wrap:false,
      section:false,
      container:false,
      scrollX:false,
    }
  },
  created: function(){


  },
  mounted: function(){
  },
  methods: {


  },
  components: {
    Navigation,
    Tag
  }
}




</script>

<style lang="scss" scoped>

@import "~/assets/scss/variable/_structure";
@import "~/assets/scss/variable/_theme";

label,input[type="checkbox"]{
  cursor: pointer;
}

.l-wrap.view,.l-container.view,.l-section.view,.l-contents.view,.l-scrollX.view{
  background-color: rgba($colorTheme,.05);
  position: relative;
  border: solid 1px rgba($colorTheme,.4);
}



</style>
