<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Component / Lists
        p.c-contentsHL__lead リストは原則ブロック要素なので、親要素の幅いっぱいに広がります。レイアウト用にもリンク用にも使えます。
        section.l-section
          h2.c-contentsHL レイアウト用
          section.l-section
            h3.c-contentsHL Free Style
            ul.c-lists.l-container
              li.c-lists__text 文字列 1行
              li.c-lists__text
                a(href="#") 文字リンク 1行
              li.c-lists__text 文字列 1行
              li.c-lists__text 文字列<br>複数行<br>複数行<br>複数行
              li.c-lists__text 文字列 1行
            .l-container
              pre.c-card.p20
                code
                    |ul.c-lists
                    |    li.c-lists__text
          section.l-section
            h3.c-contentsHL 定義リスト
            ul.c-lists.l-container
              li.c-lists__text
                dl
                  dt.c-lists__text__headline 文字列 2行
                  dd 文字列 2行
              li.c-lists__text
                dl
                  dt.c-lists__text__headline 文字列 2行
                  dd
                    a(href="#") 文字リンク 2行
              li.c-lists__text
                dl
                  dt.c-lists__text__headline 文字列 2行
                  dd 文字列 2行
            .l-container
              pre.c-card.p20
                code
                    |ul.c-lists
                    |    li.c-lists__text
                    |      dl
                    |        dt.c-lists__text__headline
                    |        dd
        section.l-section
          h2.c-contentsHL リンク用
          section.l-section
            h3.c-contentsHL 1行表示
            ul.c-lists.l-container
              li.c-lists__link
                a(href="#") リストリンク 1行
              li.c-lists__link
                a(href="#") リストリンク 1行
              li.c-lists__link
                a(href="#") リストリンク 1行
            .l-container
              pre.c-card.p20
                code
                    |ul.c-lists
                    |    li.c-lists__link
                    |      a(href="#")
            h3.c-contentsHL 1行表示(矢印付)
            ul.c-lists.l-container
              li.c-lists__link.c-lists__link_arrow
                a(href="#") リストリンク(矢印付) 1行
              li.c-lists__link.c-lists__link_arrow
                a(href="#") リストリンク(矢印付) 1行
              li.c-lists__link.c-lists__link_arrow
                a(href="#") リストリンク(矢印付) 1行
            .l-container
              pre.c-card.p20
                code
                    |ul.c-lists
                    |    li.c-lists__link.c-lists__link_arrow
                    |      a(href="#")
          section.l-section
            h3.c-contentsHL ネスト用
            ul.c-lists.l-container
              span.c-lists__headline 見出し
              li.c-lists__nest
                a(href="#") ネスト用 1行
              li.c-lists__nest
                a(href="#") ネスト用 1行
              li.c-lists__nest
                a(href="#") ネスト用 1行
            .l-container
              pre.c-card.p20
                code
                    |ul.c-lists
                    |    span.c-lists__headline 見出し
                    |    li.c-lists__nest
        section.l-section
          h2.c-contentsHL アコーディオン
          section.l-section
            h3.c-contentsHL 文字列を内包
            ul.c-lists.l-container
              li.c-lists__accordion
                input#ac-1(type="checkbox" name="ac")
                label.fB(for="ac-1") 開閉式リスト
                  p.c-lists__accordion__icon
                .c-lists__accordion__content
                  p 内容内容内容内容内容内容内容内容
                    |<br>内容内容内容内容内容内容内容内容
              li.c-lists__accordion
                input#ac-2(type="checkbox" name="ac")
                label.fB(for="ac-2") 開閉式リスト
                  p.c-lists__accordion__icon
                .c-lists__accordion__content
                  p 内容内容内容内容内容内容内容内容
                    |<br>内容内容内容内容内容内容内容内容
            .l-container
              pre.c-card.p20
                code
                    |ul.c-lists
                    |    li.c-lists__accordion
                    |        input#ac-1(type="checkbox" name="ac")
                    |        label.fB(for="ac-1") 見出し
                    |            p.c-lists__accordion__icon
                    |        .c-lists__accordion__content
                    |            p 文字列
          section.l-section
            h3.c-contentsHL リストを内包
            ul.c-lists.l-container
              li.c-lists__accordion
                input#ac-3(type="checkbox" name="ac")
                label.fB(for="ac-3") 開閉式リスト
                  p.c-lists__accordion__icon
                .c-lists__accordion__content
                  ul.c-lists
                    li.c-lists__nest
                      a(href="#") ネスト用 1行
                    li.c-lists__nest
                      a(href="#") ネスト用 1行
                    li.c-lists__nest
                      a(href="#") ネスト用 1行
              li.c-lists__accordion
                input#ac-4(type="checkbox" name="ac")
                label.fB(for="ac-4") 開閉式リスト
                  p.c-lists__accordion__icon
                .c-lists__accordion__content
                  ul.c-lists
                    li.c-lists__nest
                      a(href="#") ネスト用 1行
                    li.c-lists__nest
                      a(href="#") ネスト用 1行
                    li.c-lists__nest
                      a(href="#") ネスト用 1行
            .l-container
              pre.c-card.p20
                code
                    |ul.c-lists
                    |    li.c-lists__accordion
                    |        input#ac-1(type="checkbox" name="ac")
                    |        label.fB(for="ac-1") 見出し
                    |            p.c-lists__accordion__icon
                    |        .c-lists__accordion__content
                    |            ul.c-lists
                    |                li.c-lists__nest
                    |                    a(href="#")
        section.l-section
          h2.c-contentsHL テキスト用
          section.l-section
            h3.c-contentsHL Type disc
            ul.c-lists.l-container
              li.c-lists__disc(v-for="n in 4") 箇条書きリスト
            .l-container
              pre.c-card.p20
                code
                    |ul.c-lists
                    |    li.c-lists__disc
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
