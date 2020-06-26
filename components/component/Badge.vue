<template lang="pug">
.c-lists
  dl.l-column.l-column_nowrap.c-lists__text
    dt.w200.flex.flex-middle
      span(v-if="modifier",:class="'c-' + val + 'Badge' + ' ' + 'c-badge_' + modifier") {{val}}
      span(v-else,:class="'c-' + val + 'Badge'") {{val}}
    dd.flex.flex-middle
      pre.c-card.p20
        code(v-if="modifier")
            |span.c-{{val}}Badge.c-badge_{{modifier}}
        code(v-else)
            |span.c-{{val}}Badge
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
