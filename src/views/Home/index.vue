<template>
  <page-template>
    <template slot="header">
      <header-ui />
    </template>
    <template slot="content">
      <content-ui />
    </template>
    <template slot="footer">
      <footer-ui />
    </template>
  </page-template>
</template>

<script>
import PageTemplate from '@/templates/Page'
import HeaderUi from '@/components/ui/Header'
import ContentUi from '@/components/ui/Content'
import FooterUi from '@/components/ui/Footer'

export default {
  name: 'Home',
  components: {
    PageTemplate,
    HeaderUi,
    ContentUi,
    FooterUi
  }
}
</script>

<style lang="stylus" scoped>
@import 'styles.styl'
</style>
