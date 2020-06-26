<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Component / Headline
        p.c-contentsHL__lead ページの要件によって、それぞれの見出しスタイルを定義。
        section.l-section
          h2.c-contentsHL メインコンテンツ用
          .l-container
            h1.c-contentsHL 見出し１
            p.c-contentsHL__lead 見出し1用リード文
            .l-container
              pre.c-card.p20
                code
                    |h1.c-contentsHL 見出し１
                    |p.c-contentsHL__lead
            h2.c-contentsHL 見出し２
            p.c-contentsHL__lead 見出し2用リード文
            .l-container
              pre.c-card.p20
                code
                    |h2.c-contentsHL 見出し２
                    |p.c-contentsHL__lead
            h3.c-contentsHL 見出し３
            .l-container
              pre.c-card.p20
                code
                    |h3.c-contentsHL 見出し３
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
[class*="__column_"]{
  border: 1px solid #FFF;
  border-radius: 20px;
  padding: 10px;
  margin-bottom: 10px;
}

</style>
