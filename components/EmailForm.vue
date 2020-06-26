<template lang="pug">
form
  input.c-textField.c-textField_mail(type="email" name="mail" placeholder="Email" list="suggestions" v-model="emailValue")
  datalist#suggestions
    option(v-for="domain in domains",:value="getSuggest(domain)")
</template>
<script>
export default {
  data: function () {
    return {
      emailValue: '',
      domains: [
        "@yahoo.co.jp",
        "@gmail.com",
        "@ezweb.ne.jp",
        "@au.com",
        "@docomo.ne.jp",
        "@i.softbank.jp",
        "@softbank.ne.jp",
        "@excite.co.jp",
        "@hotmail.co.jp",
        "@hotmail.com",
        "@icloud.com",
        "@live.jp",
        "@me.com",
        "@mineo.jp",
        "@nifty.com",
        "@outlook.com",
        "@outlook.jp",
        "@yahoo.ne.jp",
        "@ybb.ne.jp",
        "@ymobile.ne.jp",
        "@aol.jp",
        "@rakuten.jp"
      ]
    }
  },
  mounted: function(){

  },
  methods: {
    getSuggest: function (domain) {
      if ((this.emailValue.match(/@/g) || []).length === 1) {
        const emailUserName = this.emailValue.split('@')[0]
        return emailUserName + domain
      } else {
        return null
      }
    }
  }
}
</script>
<style lang="scss" scoped>

</style>
