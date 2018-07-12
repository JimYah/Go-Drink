<template lang="pug">
  .container
    router-link(class="go__index", to='/')
      i(class="fas fa-arrow-left")
      span 回首頁

    .menu

      .menu__image

      .menu__content

</template>

<script>
  export default {
    data() {
      return {
        menus: [
            {
              title: '可不可',
              desc: '很好喝',
              phone: '1234567',
              zone: '西屯區',
              address: '大容東街1234567號',
              image: require('~/static/images/kebuke.jpg'),
              id: 1
            },
            {
              title: '清心',
              desc: '很好喝',
              phone: '7654321',
              zone: '西屯區',
              address: '大容東街7654321號',
              image: require('~/static/images/chingshin.jpg'),
              id: 2
            }
        ]
      }
    }
  }
</script>

<style lang="sass" scoped>
.go__index
  position: absolute
  top: 15px
  left: 15px
  color: #373737
  font-weight: bold

  i
    margin-right: 10px


.menu
  width: 760px
  // padding: 20px
  margin: 50px auto
  background-color: #FFF
  border-radius: 5px
  box-shadow: 0 5px 10px hsla(0,0%,46%,.5)
  overflow: hidden

  &__image
    width: 100%
    padding-bottom: 30%
    background: url('~/static/images/kebuke.jpg') no-repeat
    background-size: cover

  &__title
    text-align: center
    font-size: 1.5rem
    font-weight: bold
    color: #373737
    letter-spacing: 3px
</style>