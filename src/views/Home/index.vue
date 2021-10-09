<template>
  <page-template>
    <template slot="header">
      <header-ui />
    </template>
  </page-template>
</template>

<script>
import PageTemplate from '@/templates/Page'
import HeaderUi from '@/components/ui/Header'

export default {
  name: 'Home',
  components: {
    PageTemplate,
    HeaderUi
  }
}
</script>

<style lang="stylus" scoped>
@import 'styles.styl'
</style>
