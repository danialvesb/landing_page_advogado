<template>
  <div class="page-template">
      <section class="header-template">
        <slot name="header"/>
      </section>
      <section class="content-template">
        <slot name="content"/>
      </section>
      <section class="footer-template">
        <slot name="footer"/>
      </section>
  </div>
</template>

<script>
export default {
  name: 'page-template'
}
</script>

<style lang="stylus" scoped>
@import 'styles.styl'
</style>
