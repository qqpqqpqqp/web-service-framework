<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Project / Tables
        p.c-contentsHL__lead
        section.l-section
          h2.c-contentsHL 定義リスト
          .l-container 簡易的なテーブルは定義リストを使用。レスポンシブに対応。
          section.l-section
            h3.c-contentsHL 縦並べ(レスポンシブ)
            .l-container
              .p-table
                dl.p-table__body.l-column(v-for="n in 3")
                  dt.p-table__title.l-column__column_1-1-4 X行×４列の例
                  dd.p-table__description.l-column__column_1-3-4 1→3→4
                  dd.p-table__description.l-column__column_1-3-4 1→3→4
                  dd.p-table__description.l-column__column_1-3-4 1→3→4
            .l-container
              pre.c-card.p20
                code
                    |.p-table
                    |    dl.p-table__body.l-column
                    |      dt.p-table__title.l-column__column_1-1-4 X行×４列の例
                    |      dd.p-table__description.l-column__column_1-3-4 1→3→4
                    |      dd.p-table__description.l-column__column_1-3-4 1→3→4
                    |      dd.p-table__description.l-column__column_1-3-4 1→3→4
            .l-container
              .p-table
                dl.p-table__body.l-column(v-for="n in 3")
                  dt.p-table__title.l-column__column_1-3-3 X行×４列の例
                  dd.p-table__description.l-column__column_1-3-3 1→3→3
                  dd.p-table__description.l-column__column_1-3-3 1→3→3
            .l-container
              pre.c-card.p20
                code
                    |.p-table
                    |    dl.p-table__body.l-column
                    |      dt.p-table__title.l-column__column_1-3-3 X行×４列の例
                    |      dd.p-table__description.l-column__column_1-3-3 1→3→3
                    |      dd.p-table__description.l-column__column_1-3-3 1→3→3
        section.l-section
          h2.c-contentsHL テーブル
          .l-container
            p セルの多いテーブルはこちらを使用。レスポンシブ対応する場合、
             a(href="/layout") l-scrollX
             |と併用する。
          section.l-section
            h3.c-contentsHL 縦並べ
            .l-container
              table.p-table
                tr
                  th(v-for="n in 6") X列
                tr(v-for="n in 3")
                  td(v-for="n in 6") X行
            .l-container
              pre.c-card.p20
                code
                    |table.p-table
                    |    tr
                    |      th
                    |    tr
                    |      td
          section.l-section
            h3.c-contentsHL 縦並べ(線なし)
            .l-container
              table.p-table.p-table_borderless
                tr
                  th(v-for="n in 6") X列
                tr(v-for="n in 3")
                  td(v-for="n in 6") X行
            .l-container.p-table_borderless
              pre.c-card.p20
                code
                    |table.p-table.p-table_borderless
                    |    tr
                    |      th
                    |    tr
                    |      td
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
