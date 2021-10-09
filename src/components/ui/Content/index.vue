<template>
  <main class="content">
    <home-content class="section-size primary"/>
    <solutions-content class="section-size"/>
    <plans-content class="section-size primary"/>
    <differentials-content class="section-size"/>
    <abount-content class="section-size primary"/>
    <contact-content class="section-size "/>
    <fac-content class="section-size primary"/>
  </main>
</template>

<script>
import HomeContent from './components/Home'
import SolutionsContent from './components/Solutions'
import PlansContent from './components/Plans'
import DifferentialsContent from './components/Differentials'
import AbountContent from './components/Abount'
import ContactContent from './components/Contact'
import FacContent from './components/Fac'

export default {
  name: 'content-ui',
  components: {
    HomeContent,
    SolutionsContent,
    PlansContent,
    DifferentialsContent,
    AbountContent,
    ContactContent,
    FacContent
  }
}
</script>

<style lang="stylus" scoped>
@import 'styles.styl'
</style>
