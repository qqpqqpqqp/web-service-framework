<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Web Service Framework
        .c-contentsHL__lead webサービスを構築するにあたり、本プロジェクトをベースに開発することで、工数の削減や品質確保に役立ちます。また過度な制約やオプションがなく、機能拡張性や柔軟性が高く、汎用的に利用できます。
        section.l-section
          h2.c-contentsHL Nuxt.js
          .c-contentsHL__lead JavaScriptフレームワーク「
            a(href="https://ja.nuxtjs.org/" target="_blank" rel="noopener") Nuxt.js
            |」を採用。SSRに対応し、豊富なモジュールで拡張性に富んで言います。学習コストも低く、コンポーネント指向のコーディングに最適です。
        section.l-section
          h2.c-contentsHL CSS設計
          section.l-section
            h3.c-contentsHL FLOCSS
            .l-container
              p.mb6 「
                a(href="https://github.com/hiloki/flocss" target="_blank" rel="noopener") FLOCSS
                |」により、様々なメリットがあります。
              ul.c-lists.f13
                li.c-lists__disc 命名規則の品質が保たれる
                li.c-lists__disc 可読性が高い
                li.c-lists__disc 重複するコーディングがなくなる
                li.c-lists__disc 柔軟性が高く、表示崩れが起きにくい
                li.c-lists__disc サービスの要件に合わせやすい
          section.l-section
            h3.c-contentsHL Atomic Design
            .l-container FLOCSSは「
              a(href="https://app.codegrid.net/entry/2017-atomic-design-1" target="_blank" rel="noopener") Atomic Design
              |」と相性が良く、ほぼ同じ考え方で活用できます。ここではComponentレイヤーをAtomsとし、ProjectレイヤーをMolecules、Organismsとして定義しています。
        section.l-section
          h2.c-contentsHL Design System
          .c-contentsHL__lead 本プロジェクトにサービスのコンセプトや拡張したComponent等を追加してメンテナンスすることで
            a(href="https://webdesign-trends.net/entry/9068" target="_blank" rel="noopener") デザインシステム
            |として利用できます。デザインシステムの構築にかかるコストを大判に削減し、一貫したUIデザインと効率的な実装を実現します。
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
