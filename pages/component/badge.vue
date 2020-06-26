<template lang="pug">
  #app
    Navigation
    main.l-contents
      .l-wrap
        h1.c-contentsHL Component / Badge
        p.c-contentsHL__lead バッジスタイルは原則、押下不可。スタイルを変更する際は、ボタンと兼用している部分があるので注意。
        section.l-section
          h2.c-contentsHL １行表示
          section.l-section
            h3.c-contentsHL Standard
            Badge(:val="val",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Standard / Square
            Badge(:val="val",:modifier="'square'",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Standard / Sub Color
            Badge(:val="val",:modifier="'orange'",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Outlined
            Badge(:val="val",:modifier="'outlined'",v-for="val in size",:key="val")
          section.l-section
            h3.c-contentsHL Circle
            Badge(:val="val",:modifier="'circle'",v-for="val in size",:key="val")
</template>

<script>
import Navigation from '~/components/Navigation.vue'
import Badge from '~/components/component/Badge.vue'
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
    Badge
  }
}




</script>

<style lang="scss" scoped>

</style>
