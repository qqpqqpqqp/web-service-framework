<template lang="pug">
  div
    span.c-smallBadge.c-badge_square {{box}}
    span.c-smallBadge.c-badge_square /{{box}}
</template>
<script>
export default {
  data: function () {
    return {
    }
  },
  props: ['box']
}
</script>
<style lang="scss" scoped>

[class*="badge_"]{
  position: absolute;
  z-index: 6000;
  &:first-child{
    top: 0;
    left: 0;
  }
  &:nth-of-type(2){
    bottom: 0;
    right: 0;
  }
}
</style>
