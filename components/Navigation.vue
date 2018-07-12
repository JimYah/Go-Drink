<template lang="pug">
.header
  .navigation
    .navigation__logo
      a(class="link", href='/')
        h1.logo GoParty
    .navigation__login
      a(class="link", href='/')
        p(class="login") 登入
</template>

<script>
  export default {

  }
</script>

<style lang="sass" scoped>
.header
  position: fixed
  top: 0
  left: 0
  width: 100%
  z-index: 999

.navigation
  position: relative
  display: flex
  width: 80%
  height: 70px
  margin: 0 auto
  align-items: center
  justify-content: center
  &__logo
    .logo
      font-size: 1.8rem
      color: #fff
      transition: all .3s ease
      &:hover
        color: rgb(251, 226, 81)
  &__login
    position: absolute
    right: 0
    top: 0
    line-height: 70px
    .login
      color: #fff
      font-size: 1.2rem
      transition: all .3s ease
      &:hover
        color: rgb(251, 226, 81)
</style>