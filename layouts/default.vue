<template>
  <div>
    <!-- <Navigation v-if="routeName === 'index'"></Navigation> -->
    <nuxt/>
  </div>
</template>

<script>
import Navigation from '~/components/Navigation.vue'

export default {
  computed: {
    routeName() {
      return this.$route.name
    }
  },
  components: {
    Navigation
  }
}
</script>

<style lang="scss">

</style>
