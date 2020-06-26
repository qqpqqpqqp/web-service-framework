<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Component / Form
        p.c-contentsHL__lead スタイル。
        section.l-section
          h2.c-contentsHL Text Field
          .l-container 横いっぱいに広がる
          section.l-section
            h3.c-contentsHL Plane
            form.l-container
              input.c-textField(type="text" name="plane" placeholder="Text Field")
            .l-container
              pre.c-card.p20
                code
                    |form
                    |    input.c-textField(type="text" name="plane" placeholder="Text Field")
          section.l-section
            h3.c-contentsHL Email
            .l-container ユーザーがフォームに文字入力時に@とそれ以降の入力を検知し、主要ドメインをサジェストします。
            EmailForm.l-container
            .l-container
              .l-scrollX.l-column.l-column_nowrap
                pre.c-card.p20.mr10.l-column__column_shrink
                  code
                      |//html
                      |EmailForm
                pre.c-card.p20.mr10.l-column__column_shrink
                  code
                      |//script
                      |import EmailForm from '~/components/EmailForm.vue'
                pre.c-card.p20.l-column__column_shrink
                  code
                      |//script
                      |export default {
                      |    components: {
                      |        EmailForm
                      |    }
                      |}
          section.l-section
            h3.c-contentsHL Password
            form.l-container
              input.c-textField.c-textField_key(type="password" name="key" placeholder="Password")
            .l-container
              pre.c-card.p20
                code
                    |form
                    |    input.c-textField.c-textField_key(type="password" name="key" placeholder="Password")
          section.l-section
            h3.c-contentsHL Search
            form.l-container
              input.c-textField.c-textField_search(type="search" name="search" placeholder="Search")
            .l-container
              pre.c-card.p20
                code
                    |form
                    |    input.c-textField.c-textField_search(type="search" name="search" placeholder="Search")
          section.l-section
            h3.c-contentsHL Plane + Small Size
            form.l-container
              input.c-textField.c-textField_small(type="text" name="plane" placeholder="Text Field")
            .l-container
              pre.c-card.p20
                code
                    |form
                    |    input.c-textField.c-textField_small(type="text" name="plane" placeholder="Text Field")
</template>

<script>
import Navigation from '~/components/Navigation.vue'
import EmailForm from '~/components/EmailForm.vue'
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
    Navigation,
    EmailForm
  }
}

</script>

<style lang="scss" scoped>

</style>
