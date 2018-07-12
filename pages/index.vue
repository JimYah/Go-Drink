<template lang="pug">
  .container
    .main__wrap
      .filters

      .shops
        .shop(
          v-for="shop in shops",
          :key="shop.title"
        )
          router-link(
            :to="`menu/?shop=${shop.id}`"
          )
            .shop__image(
              :style="`background-image: url(${shop.image})`"
            )
            .shop__detail
              h3(
                class="shop__detail__title",
                v-text="shop.title"
              )
              p(
                class="shop__detail__zone",
                v-text="shop.zone"
              )
              p(
                class="shop__detail__address"
                v-text="shop.address"
              )

</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  data() {
    return {
      shops: [
          {
            title: '可不可',
            desc: '很好喝',
            phone: '1234567',
            zone: '西屯區',
            address: '大容東街 1234567 號',
            image: require('~/static/images/kebuke.jpg'),
            id: 1
          },
          {
            title: '清心',
            desc: '很好喝',
            phone: '7654321',
            zone: '西屯區',
            address: '大容東街 7654321 號',
            image: require('~/static/images/chingshin.jpg'),
            id: 2
          }
      ]
    }
  },
  components: {
    AppLogo
  }
}
</script>

<style lang="sass" scope>
  .main__wrap
    display: flex
    align-items: flex-start
    width: 960px
    margin: 0px auto

    .filters
      position: sticky
      top: 50px
      width: 260px
      margin: 0 20px 0 0
      border: 1px solid #987654

    .shops
      width: 100%
      display: flex
      align-items: center
      justify-content: flex-start
      flex: 1

      .shop
        width: 49%
        margin-bottom: 25px
        background-color: #FFF
        transition: all .3s ease
        border-radius: 5px
        overflow: hidden

        &:hover
          box-shadow: 0 5px 10px hsla(0,0%,46%,.5)
          transform: translateY(-3px)

        &:nth-child(2n+1)
          margin-right: 2%

        &__image
          width: 100%
          padding-bottom: 60%
          background-repeat: no-repeat
          background-size: cover
          background-position: center

        &__detail
          padding: 10px
          color: #4a4a4a

          &__title
            font-size: 1.2rem
            font-weight: bold

          &__zone
            display: inline-block
            padding: 5px 10px
            margin: 20px 0
            font-size: .7rem
            color: #F2F2F2
            border-radius: 5px
            background: #4A90E2

          &__address
            font-weight: 500px
</style>
