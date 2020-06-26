<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Project / Cards
        p.c-contentsHL__lead カードはサービスの要件によって表示要素が大きく変化します。基本的なスタイルはComponentを利用し、必要に応じてProjectで定義する。
        section.l-section
          h2.c-contentsHL カード(全体リンク)
          section.l-section
            h3.c-contentsHL Regular size
            a.c-card.p-card.p-card_regular.mr10
              .p-card__frame.p-card__frame_16x9
                img(src="~/assets/images/image.jpg" srcset="~/assets/images/image.jpg 1x,~/assets/images/image@2x.jpg 2x" alt="画像")
              section.p-card__contents
                h4.p-card__headline カードタイトル
                p.p-card__text カード内容
            a.c-card.p-card.p-card_regular
              .p-card__frame.p-card__frame_16x9
                img(src="~/assets/images/image.jpg" srcset="~/assets/images/image.jpg 1x,~/assets/images/image@2x.jpg 2x" alt="画像")
              section.p-card__contents
                h4.p-card__headline カードタイトル
                p.p-card__text カード内容
          section.l-section
            h3.c-contentsHL small size
            a.c-card.mr10
              .p-card__frame.p-card__frame_16x9
                img(src="~/assets/images/image.jpg" srcset="~/assets/images/image.jpg 1x,~/assets/images/image@2x.jpg 2x" alt="画像")
              section.p-card__contents
                h4.p-card__headline カードタイトル
                p.p-card__text カード内容
            a.c-card
              .p-card__frame.p-card__frame_16x9
                img(src="~/assets/images/image.jpg" srcset="~/assets/images/image.jpg 1x,~/assets/images/image@2x.jpg 2x" alt="画像")
              section.p-card__contents
                h4.p-card__headline カードタイトル
                p.p-card__text カード内容
          hr
        section.l-section
          h2.c-contentsHL カード(全体リンクなし)
          section.l-section
            h3.c-contentsHL Regular size
            .c-card.p-card.p-card_regular.mr10
              .p-card__frame.p-card__frame_16x9
                img(src="~/assets/images/image.jpg" srcset="~/assets/images/image.jpg 1x,~/assets/images/image@2x.jpg 2x" alt="画像")
              section.p-card__contents
                h4.p-card__headline カードタイトル
                p.p-card__text カード内容。
                  a(href="#") リンク文字
          section.l-section
            h3.c-contentsHL Regular size(ボタン付き)
            .l-column
              .c-card.p-card.p-card_regular.mr10
                .p-card__frame.p-card__frame_16x9
                  img(src="~/assets/images/image.jpg" srcset="~/assets/images/image.jpg 1x,~/assets/images/image@2x.jpg 2x" alt="画像")
                section.p-card__contents
                  h4.p-card__headline カードタイトル
                  p.p-card__text カード内容。
                .p-card__buttonArea
                  a.c-regularButton.c-button_text ボタン
</template>
<script>
import Navigation from '~/components/Navigation.vue'
export default {
  data: function () {
    return {
    }
  },
  created: function(){


  },
  mounted: function(){
  },
  methods: {


  },
  components: {
    Navigation
  }
}




</script>

<style lang="scss" scoped>


</style>
