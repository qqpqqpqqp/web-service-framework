<template lang="pug">
.l-navigation
  header.l-header.l-wrap.l-wrap_header
    .p-drawer__menuBtn(:class="{'p-drawer__menuBtn_open': drawr}" @click='drawr =! drawr')
      span
    Logo.l-header__logo
    form.l-header__search
      input.c-textField.c-textField_search.c-textField_small(type="text" name="search" placeholder="Sample Form")
    nav.p-drawer(:class="{'p-drawer_open': drawr}" role="navigation")
      .p-drawer__logo
        Logo
      ul.c-lists.p-drawer__scrollArea
        li.c-lists__link.c-lists__link_arrow
          a(href="/start") Start
        li.c-lists__link.c-lists__link_arrow
          a(href="/theme") Theme
        li.c-lists__text
          span.c-lists__headline Layout
          ul.c-lists
            li.c-lists__nest
              a(href="/layout/") Layout
            li.c-lists__nest
              a(href="/layout/column") Column
        li.c-lists__text
          span.c-lists__headline Component
          ul.c-lists
            li.c-lists__nest
              a(href="/component/button") Button
            li.c-lists__nest
              a(href="/component/badge") Badge
            li.c-lists__nest
              a(href="/component/headline") Headline
            li.c-lists__nest
              a(href="/component/lists") Lists
            li.c-lists__nest
              a(href="/component/cards") Cards
            li.c-lists__nest
              a(href="/component/form") Form
        li.c-lists__text
          span.c-lists__headline Project
          ul.c-lists
            li.c-lists__nest
              a(href="/project/cards") Cards
            li.c-lists__nest
              a(href="/project/table") Tables
            li.c-lists__nest
              a(href="/project/drawer") Drawer
        li.c-lists__link.c-lists__link_arrow.mb40
          a(href="/utility/") Utility
    .p-drawer__scrim(@click='drawr = false')
</template>
<script>
import Logo from '~/components/Logo.vue'
export default {
  data: function () {
    return {
      drawr:false,
    }
  },
  mounted: function(){
    window.addEventListener('resize', this.clearDrawr);
  },
  methods: {
    clearDrawr: function () {
      this.drawr = false; //ドロワーを閉じる
    }
  },
  components: {
    Logo
  }
}
</script>
<style lang="scss" scoped>
// ★変数一覧 ★★★★★★★★★★★★★★★★★★
@import "../assets/scss/variable/structure";
@import "~/assets/scss/variable/_theme";


// ★ヘッダーナビ ★★★★★★★★★★★★★★★★★★
//関連例の高い .l-headerは Layout Layer に記述
.p-drawer{
  position: fixed;
  z-index: 5300;
  top: 0;
  left: -#{$drawerWidth};
  width: $drawerWidth;
  height: 100%;
  overflow-y: hidden;
  background-color: $drawerBg;
  padding: 50px 0 0 0; //スマホメニュー上部余白
  transition: all 0.2s;
  box-shadow: 0px 3px 1px -2px rgba(0, 0, 0, 0.2),0px 2px 2px 0px rgba(0, 0, 0, 0.14),0px 1px 5px 0px rgba(0,0,0,.12);
  @include mq(pc){
    left: 0;
    padding-top: 0;
  }
  @include mq(max){
    position: absolute;
    height: 100vh;
    transition:none;
  }
  &_open{
    left: 0;
    & + .p-drawer__scrim{
      display: block;
    }
  }
  &__scrollArea{
    overflow-y: scroll;
    height: calc(100vh - 100px);
    @include mq(pc){
      -ms-overflow-style: none;    /* IE, Edge 対応 */
      scrollbar-width: none;       /* Firefox 対応 */
    }
  }
  &__menuBtn{
    position: relative;
    display: block;
    z-index: 5301;
    height: 36px;
    width: 30px;
    min-width: 30px;
    padding: 0px 4px;
    margin-right: 16px;
    cursor: pointer;
    @include mq(pc){
      display: none;
    }
    & > span,span:before,span:after{
      height: 2px;
      width: 100%;
      background-color: #fff;
      transition: all 0.6s cubic-bezier(0.19, 1, 0.22, 1);
    }
    & > span,span:before,span:after{
      position: absolute;
      content: " ";
      left: 0;
    }
    & > span{
      display: inline-block;
      position: relative;
      &:before{
        top: -8px;
      }
      &:after{
        top: 8px;
      }
    }
    & + .p-drawer {
      margin-left: 0;
    }
    &_open{
      & > span{
        top: 0;
        background-color: transparent;
        &:before{
          top: 0;
          transform: rotate(45deg);
        }
        &:after{
          top: 0;
          transform: rotate(-45deg);
        }
      }
    }
  }
  &__scrim{
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 5;
    background-color: rgba(darken($colorBase,10%),.6);
  }
  &__logo{
    display: none;
    @include mq(pc){
      display: flex;
      align-items: center;
      justify-content:center;
      height: 100px;
    }
  }
}




</style>
