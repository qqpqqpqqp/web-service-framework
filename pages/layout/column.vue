<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Layout / Column
        .c-contentsHL__lead カラムレイアウトに使用。レスポンシブ対応可能。このページでは可視化する為にスタイル(枠線・余白)を適用しているが、デフォルトでは汎用的に使えるように装飾のスタイルは無い。
        section.l-section
          h2.c-contentsHL レスポンシブ
          section.l-section
            h3.c-contentsHL windowの幅：{{width}}px
            .p-table.l-column
              dl.l-column__column_four
                dt SP
                dd.sp 0~375px
              dl.l-column__column_four
                dt Tablet
                dd.tb 376~767px
              dl.l-column__column_four
                dt PC
                dd.pc  768px~1279px
              dl.l-column__column_four
                dt MAX
                dd.max 1280px~
          section.l-section
            h3.c-contentsHL SP(3カラム)→Tablet(4カラム)→PC(5カラム)
            .l-column.l-container
              .l-column__column_3-4-5.c-card.p10.b1 column (3→4→5)
              .l-column__column_3-4-5.c-card.p10.b1 column (3→4→5)
              .l-column__column_3-4-5.c-card.p10.b1 column (3→4→5)
              .l-column__column_3-4-5.c-card.p10.b1 column (3→4→5)
              .l-column__column_3-4-5.c-card.p10.b1 column (3→4→5)
            .l-container
              pre.c-card.p20
                code
                    |.l-column
                    |    .l-column__column_3-4-5
                    |    .l-column__column_3-4-5
                    |    .l-column__column_3-4-5
                    |    .l-column__column_3-4-5
                    |    .l-column__column_3-4-5
          section.l-section
            h3.c-contentsHL SP(2カラム)→Tablet(3カラム)→PC(4カラム)
            .l-column.l-container
              .l-column__column_2-3-4.c-card.p10.b1 column (2→3→4)
              .l-column__column_2-3-4.c-card.p10.b1 column (2→3→4)
              .l-column__column_2-3-4.c-card.p10.b1 column (2→3→4)
              .l-column__column_2-3-4.c-card.p10.b1 column (2→3→4)
            .l-container
              pre.c-card.p20
                code
                    |.l-column
                    |    .l-column__column_2-3-4
                    |    .l-column__column_2-3-4
                    |    .l-column__column_2-3-4
                    |    .l-column__column_2-3-4
          section.l-section
            h3.c-contentsHL SP(1カラム)→Tablet(2カラム)→PC(3カラム)
            .l-column.l-container
              .l-column__column_1-2-3.c-card.p10.b1 column (1→2→3)
              .l-column__column_1-2-3.c-card.p10.b1 column (1→2→3)
              .l-column__column_1-2-3.c-card.p10.b1 column (1→2→3)
            .l-container
              pre.c-card.p20
                code
                    |.l-column
                    |    .l-column__column_1-2-3
                    |    .l-column__column_1-2-3
                    |    .l-column__column_1-2-3
        section.l-section
          h2.c-contentsHL カラム数固定
          section.l-section
            h3.c-contentsHL 数指定
            .l-column.l-container
              .l-column__column_one.c-card.p10.b1 １つ
              .l-column__column_two.c-card.p10.b1(v-for="n in 2") ２つ
              .l-column__column_three.c-card.p10.b1(v-for="n in 3") ３つ
              .l-column__column_four.c-card.p10.b1(v-for="n in 4") ４つ
              .l-column__column_five.c-card.p10.b1(v-for="n in 5") ５つ
              .l-column__column_six.c-card.p10.b1(v-for="n in 6") ６つ
              .l-column__column_seven.c-card.p10.b1(v-for="n in 7") ７つ
              .l-column__column_eight.c-card.p10.b1(v-for="n in 8") ８つ
              .l-column__column_nine.c-card.p10.b1(v-for="n in 9") ９つ
              .l-column__column_ten.c-card.p10.b1(v-for="n in 10") １０
            .l-container
              pre.c-card.p20
                code
                    |.l-column
                    |   .l-column__column_one １つ
                    |   .l-column__column_two ２つ
                    |   .l-column__column_three ３つ
                    |   .l-column__column_four ４つ
                    |   .l-column__column_five ５つ
                    |   .l-column__column_six ６つ
                    |   .l-column__column_seven ７つ
                    |   .l-column__column_eight ８つ
                    |   .l-column__column_nine ９つ
                    |   .l-column__column_ten １０
        section.l-section
          h2.c-contentsHL カラム数未指定
          section.l-section
            h3.c-contentsHL カラム落ちあり
            .l-column.l-container
              .c-card.p10.b1(v-for="n in 10") 内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            .l-container
              pre.c-card.p20
                code
                    |.l-column
          section.l-section
            h3.c-contentsHL カラム落ちなし
            .l-column.l-column_nowrap.l-container
              .c-card.p10.b1(v-for="n in 10") 内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            .l-container
              pre.c-card.p20
                code
                    |.l-column.l-column_nowrap
          section.l-section
            h3.c-contentsHL カラム落ちなし(均等)
            .l-column.l-column_nowrap.l-container
              .l-column__column_grow.c-card.p10.b1(v-for="n in 3") 内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容
            .l-container
              pre.c-card.p20
                code
                    |.l-column.l-column_nowrap
                    |   .l-column__column_grow
          section.l-section
            h3.c-contentsHL カラム落ちなし(等倍)
            .l-column.l-column_nowrap.l-container
              .l-column__column_shrink.c-card.p10.b1(v-for="n in 3") 内容内容内容容内容内容内容内容内容内容内容内容内容
            .l-container
              pre.c-card.p20
                code
                    |.l-column.l-column_nowrap
                    |   .l-column__column_shrink
        section.l-section
          h2.c-contentsHL flex-box
          section.l-section
            h3.c-contentsHL 2カラム + 片方固定幅
            .l-column.l-column_nowrap.l-container
              .c-card.p10.b1.w200 幅200px固定
              .l-column__column_grow.c-card.p10.b1 可変幅
            .l-container
              pre.c-card.p20
                code
                    |.l-column.l-column_nowrap
                    |   .w200
                    |   .l-column__column_grow
</template>

<script>
import Navigation from '~/components/Navigation.vue'
export default {
  data: function () {
    if (process.browser){
      var width = self.innerWidth;
    }
    return {
      width: width
    }
  },
  created: function(){
  },
  mounted: function(){
    this.getWidth();
    window.addEventListener('resize', this.getWidth);
  },
  methods: {
    getWidth: function () {
      //幅を再取得
      this.width = self.innerWidth;
    }
  },
  components: {
    Navigation
  }
}




</script>

<style lang="scss" scoped>

@import "~/assets/scss/variable/_structure";
@import "~/assets/scss/variable/_theme";


@include mq(sp){
  .sp{
    background-color: rgba($colorTheme,.3);
  }
}
@include mq(tb){
  .tb{
    background-color: rgba($colorTheme,.3);
  }
}
@include mq(pc){
  .tb{
    background:none;
  }
  .pc{
    background-color: rgba($colorTheme,.3);
  }
}
@include mq(max){
  .pc{
    background:none;
  }
  .max{
    background-color: rgba($colorTheme,.3);
  }
}


</style>
