<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Component / Button
        p.c-contentsHL__lead ボタンスタイルは原則、&#12296;a&#12297;タグに付与する。スタイルを変更する際は、バッジと兼用している部分があるので注意。
        section.l-section
          h2.c-contentsHL １行表示
          section.l-section
            h3.c-contentsHL Standard
            Button(:val="val",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Standard / Square
            Button(:val="val",:modifier="'square'",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Standard / Sub Color
            Button(:val="val",:modifier="'orange'",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Outlined
            Button(:val="val",:modifier="'outlined'",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Disabled
            Button(:val="val",:modifier="'disabled'",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Circle
            Button(:val="val",:modifier="'circle'",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Text
            Button(:val="val",:modifier="'text'",v-for="val in size",:key="val")
        section.l-section
          h2.c-contentsHL ２行表示
          section.l-section
            h3.c-contentsHL Standard
            Button(:val="val",:modifier="'2line'",v-for="val in size",:key="val")
</template>

<script>
import Navigation from '~/components/Navigation.vue'
import Button from '~/components/component/Button.vue'
export default {
  data: function () {
    return {
      size:['small','regular','large','xlarge','xxlarge']
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
    Button
  }
}




</script>

<style lang="scss" scoped>

[class*="__column_"] p{
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  align-items: center;
  height: 80px;
  margin-bottom: 8px;
}

</style>
