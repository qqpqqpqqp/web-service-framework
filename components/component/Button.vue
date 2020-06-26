<template lang="pug">
.c-lists
  dl.l-column.l-column_nowrap.c-lists__text
    dt.w200.flex.flex-middle
      a(v-if="modifier == '2line'",:class="'c-' + val + 'Button'")
        dl
          dt {{val}}
          dd ボタン
      a(v-else-if="modifier",:class="'c-' + val + 'Button' + ' ' + 'c-button_' + modifier") {{val}}
      a(v-else,:class="'c-' + val + 'Button'") {{val}}
    dd.flex.flex-middle
      pre.c-card.p20
        code(v-if="modifier == '2line'")
            |a.c-{{val}}Button
            |   dl
            |     dt {{val}}
            |     dd ボタン
        code(v-else-if="modifier")
            |a.c-{{val}}Button.c-button_{{modifier}}
        code(v-else)
            |a.c-{{val}}Button
</template>
<script>
export default {
  data: function () {
    return {
    }
  },
  props: ['val','modifier']
}
</script>
<style lang="scss" scoped>

</style>
