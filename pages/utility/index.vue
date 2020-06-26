<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Utility
        p.c-contentsHL__lead 補助的に
        section.l-section
          h2.c-contentsHL 余白系
          section.l-section
            h3.c-contentsHL Margin
            .l-scrollX
              table.p-table
                tr
                  th プロパティ
                  th クラス名/接頭辞
                  th クラス名/値
                  th クラス例
                  th 効果
                tr
                  td margin
                  td m
                  td(rowspan="7") 2~60<br>(2の倍数のみ)
                  td
                    pre.c-card.pX20.pY10
                      code span.m10
                  td 外余白
                tr
                  td margin-top
                  td mt
                  td
                    pre.c-card.pX20.pY10
                      code span.mt10
                  td 上側に外余白
                tr
                  td margin-right
                  td mr
                  td
                    pre.c-card.pX20.pY10
                      code span.mr10
                  td 右側に外余白
                tr
                  td margin-bottom
                  td mb
                  td
                    pre.c-card.pX20.pY10
                      code span.mb10
                  td 下側に外余白
                tr
                  td margin-left
                  td ml
                  td
                    pre.c-card.pX20.pY10
                      code span.ml10
                  td 左側に外余白
                tr
                  td margin-top<br>margin-bottom
                  td mY
                  td
                    pre.c-card.pX20.pY10
                      code span.mY10
                  td 上下に外余白
                tr
                  td(rowspan="2") margin-right<br>margin-left
                  td(rowspan="2") mX
                  td
                    pre.c-card.pX20.pY10
                      code span.mX10
                  td 左右に外余白
                tr
                  td 0auto
                  td
                    pre.c-card.pX20.pY10
                      code div.mX0auto
                  td 中央寄せ
          section.l-section
            h3.c-contentsHL Padding
            .l-scrollX
              table.p-table
                tr
                  th プロパティ
                  th クラス名/接頭辞
                  th クラス名/値
                  th クラス例
                  th 効果
                tr
                  td padding
                  td p
                  td(rowspan="7") 2~60<br>(2の倍数のみ)
                  td
                    pre.c-card.pX20.pY10
                      code span.p10
                  td 内余白
                tr
                  td padding-top
                  td pt
                  td
                    pre.c-card.pX20.pY10
                      code span.pt10
                  td 上側に内余白
                tr
                  td padding-right
                  td pr
                  td
                    pre.c-card.pX20.pY10
                      code span.pr10
                  td 右側に内余白
                tr
                  td padding-bottom
                  td pb
                  td
                    pre.c-card.pX20.pY10
                      code span.pb10
                  td 下側に内余白
                tr
                  td padding-left
                  td pl
                  td
                    pre.c-card.pX20.pY10
                      code span.pl10
                  td 左側に内余白
                tr
                  td padding-top<br>padding-bottom
                  td pY
                  td
                    pre.c-card.pX20.pY10
                      code span.pY10
                  td 上下に内余白
                tr
                  td padding-right<br>padding-left
                  td pX
                  td
                    pre.c-card.pX20.pY10
                      code span.pX10
                  td 左右に内余白
        section.l-section
          h2.c-contentsHL 文字系
          section.l-section
            h3.c-contentsHL Font
            .l-scrollX
              table.p-table
                tr
                  th プロパティ
                  th クラス名/接頭辞
                  th クラス名/値
                  th クラス例
                  th 効果
                tr
                  td(rowspan="4") font-size
                  td(rowspan="6") f
                  td 8~60<br>(2の倍数のみ)
                  td
                    pre.c-card.pX20.pY10
                      code span.f10
                  td.f10 フォントサイズ指定
                tr
                  td 5
                  td
                    pre.c-card.pX20.pY10
                      code span.f5
                  td.f5 超極小文字
                tr
                  td 11
                  td
                    pre.c-card.pX20.pY10
                      code span.f11
                  td.f11 小さめ文字
                tr
                  td 13
                  td
                    pre.c-card.pX20.pY10
                      code span.f13
                  td.f13 若干小さい文字
                tr
                  td(rowspan="2") font-weight
                  td B
                  td
                    pre.c-card.pX20.pY10
                      code span.fB
                  td.fB bold
                tr
                  td L
                  td
                    pre.c-card.pX20.pY10
                      code span.fL
                  td.fL lighter
                tr
                  td(rowspan="3") font-family
                  td(rowspan="3") -
                  td mincho
                  td
                    pre.c-card.pX20.pY10
                      code span.mincho
                  td.mincho 明朝体
                tr
                  td serif
                  td
                    pre.c-card.pX20.pY10
                      code span.serif
                  td.serif serif
                tr
                  td roboto
                  td
                    pre.c-card.pX20.pY10
                      code span.roboto
                  td.roboto roboto
          section.l-section
            h3.c-contentsHL Text
            .l-scrollX
              table.p-table
                tr
                  th プロパティ
                  th クラス名/接頭辞
                  th クラス名/値
                  th クラス例
                  th.w150 効果
                tr
                  td(rowspan="6") line-height
                  td(rowspan="6") lh
                  td 10
                  td
                    pre.c-card.pX20.pY10
                      code p.lh10
                  td.lh10 1em分<br>1em分
                tr
                  td 13
                  td
                    pre.c-card.pX20.pY10
                      code p.lh13
                  td.lh13 1.3em分<br>1.3em分
                tr
                  td 15
                  td
                    pre.c-card.pX20.pY10
                      code p.lh15
                  td.lh15 1.5em分<br>1.5em分
                tr
                  td 18
                  td
                    pre.c-card.pX20.pY10
                      code p.lh18
                  td.lh18 1.8em分<br>1.8em分
                tr
                  td 20
                  td
                    pre.c-card.pX20.pY10
                      code p.lh20
                  td.lh20 2em分<br>2em分
                tr
                  td 30
                  td
                    pre.c-card.pX20.pY10
                      code p.lh30
                  td.lh30 3em分<br>3em分
                tr
                  td(rowspan="4") text-align
                  td(rowspan="4") ta
                  td C
                  td
                    pre.c-card.pX20.pY10
                      code p.taC
                  td.taC 中央揃え
                tr
                  td L
                  td
                    pre.c-card.pX20.pY10
                      code p.taL
                  td.taL 左揃え
                tr
                  td R
                  td
                    pre.c-card.pX20.pY10
                      code p.taR
                  td.taR 右揃え
                tr
                  td J
                  td
                    pre.c-card.pX20.pY10
                      code p.taJ
                  td.taJ 正当化abc def ghi jkl mno pqrs tuv wxyz
        section.l-section
          h2.c-contentsHL レイアウト系
          section.l-section
            h3.c-contentsHL Width & height
            .l-scrollX
              table.p-table
                tr
                  th プロパティ
                  th クラス名/接頭辞
                  th クラス名/値
                  th クラス例
                  th 効果
                tr
                  td(rowspan="2") width
                  td(rowspan="2") w
                  td 10~640<br>(2の倍数のみ)
                  td
                    pre.c-card.pX20.pY10
                      code p.w10
                  td 固定幅指定
                tr
                  td 5p~100p<br>(5の倍数のみ)
                  td
                    pre.c-card.pX20.pY10
                      code p.w10p
                  td 割合幅指定
                tr
                  td height
                  td h
                  td 10~240<br>(2の倍数のみ)
                  td
                    pre.c-card.pX20.pY10
                      code p.h10
                  td 固定高さ指定
          section.l-section
            h3.c-contentsHL flex box(親)
            .l-scrollX
              table.p-table
                tr
                  th プロパティ
                  th クラス名/接頭辞
                  th クラス名/値
                  th クラス例
                  th 効果
                tr
                  td display
                  td flex
                  td -
                  td
                    pre.c-card.pX20.pY10
                      code div.flex
                  td display:flex;
                tr
                  td flex-flow
                  td(rowspan="8") flex-
                  td wrap
                  td
                    pre.c-card.pX20.pY10
                      code div.flex.flex-wrap
                  td カラム落ちあり
                tr
                  td(rowspan="5") justify-content
                  td between
                  td
                    pre.c-card.pX20.pY10
                      code div.flex.flex-between
                  td space-between
                tr
                  td around
                  td
                    pre.c-card.pX20.pY10
                      code div.flex.flex-around
                  td space-around
                tr
                  td center
                  td
                    pre.c-card.pX20.pY10
                      code div.flex.flex-center
                  td 横方向中央
                tr
                  td right
                  td
                    pre.c-card.pX20.pY10
                      code div.flex.flex-right
                  td 右寄せ
                tr
                  td left
                  td
                    pre.c-card.pX20.pY10
                      code div.flex.flex-left
                  td 左寄せ
                tr
                  td(rowspan="2") align-items
                  td middle
                  td
                    pre.c-card.pX20.pY10
                      code div.flex.flex-middle
                  td 縦方向中央
                tr
                  td stretch
                  td
                    pre.c-card.pX20.pY10
                      code div.flex.flex-stretch
                  td stretch
          section.l-section
            h3.c-contentsHL flex box(子)
            .l-scrollX
              table.p-table
                tr
                  th プロパティ
                  th クラス名/接頭辞
                  th クラス名/値
                  th クラス例
                  th 効果
                tr
                  td margin-right
                  td(rowspan="3") flex-child-
                  td left
                  td
                    pre.c-card.pX20.pY10
                      code
                        |ul.flex
                        |   li.flex-child-left
                  td 子要素を左寄せ
                tr
                  td margin-left
                  td right
                  td
                    pre.c-card.pX20.pY10
                      code
                        |ul.flex
                        |   li.flex-child-right
                  td 子要素を右寄せ
                tr
                  td flex-grow
                  td grow
                  td
                    pre.c-card.pX20.pY10
                      code
                        |ul.flex
                        |   li.flex-child-grow
                  td 子要素が広がる or 均等
</template>
<script>
import Navigation from '~/components/Navigation.vue'
export default {
  data: function () {
    return {
    }
  },
  components: {
    Navigation
  }
}




</script>

<style lang="scss" scoped>



</style>
