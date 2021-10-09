<template>
  <header class="header">
    <brand-ui />
    <menu-ui />
  </header>
</template>

<script>
import MenuUi from '@components/ui/Menu'
import BrandUi from '@components/ui/Brand'

export default {
  name: 'header-ui',
  components: {
    MenuUi,
    BrandUi
  }
}
</script>

<style lang="stylus" scoped>
@import 'styles.styl'
</style>
