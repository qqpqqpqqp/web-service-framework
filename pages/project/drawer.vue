<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Project / Drawer
        p.c-contentsHL__lead Global Navigationに利用。サイト導線の根幹なので基本的には全ページに配置を想定。
        section.l-section
          h2.c-contentsHL Side Menu Type
          .l-container
            p SP(収納) → Tablet(収納) →  PC(表示)
            p PC版で上部ナビゲーションに可変したい場合は、修正が必要です。
          .l-container
            .l-scrollX.l-column.l-column_nowrap
              pre.c-card.p20.mr10.l-column__column_shrink
                code
                    |//html
                    |#app
                    |   Navigation
                    |   main.l-contents
              pre.c-card.p20.mr10.l-column__column_shrink
                code
                    |//script
                    |import Navigation from '~/components/Navigation.vue'
              pre.c-card.p20.l-column__column_shrink
                code
                    |//script
                    |export default {
                    |    components: {
                    |        Navigation
                    |    }
                    |}
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
