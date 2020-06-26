<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Component / Cards
        p.c-contentsHL__lead カードはサービスの要件によって表示要素が大きく変化するのでComponentにおいては基本的なスタイルのみにとどめ、詳細はProjectにおいて定義する。
        section.l-section
          h2.c-contentsHL カード(全体リンク)
          section.l-section
            h3.c-contentsHL Regular size
            .l-column
              a.c-card.mr10
                p.p16 カード
              a.c-card
                p.p16 カード
          hr
        section.l-section
          h2.c-contentsHL カード(全体リンクなし)
          section.l-section
            h3.c-contentsHL Free size
            .l-column
              .c-card
                p.p16 カード
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
