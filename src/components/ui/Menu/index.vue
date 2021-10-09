<template>
  <nav class="menu">
    <a
      @click="setActiveOption(option.name)"
      :ref="option.name"
      v-for="(option, index) in options"
      :key="index"
    >
      {{ option.label }}
    </a>
  </nav>
</template>

<script>
export default {
  name: 'menu-ui',
  methods: {
    setActiveOption (name) {
      this.active = name
    }
  },
  watch: {
    active (newValue, oldValue) {
      this.$refs[newValue][0].classList.add('a-visited')

      if (oldValue) {
        this.$refs[oldValue][0].classList.remove('a-visited')
      }
    }
  },
  mounted () {
    this.setActiveOption('home')
  },
  data: () => ({
    active: '',
    options: [
      {
        name: 'home',
        label: 'Home'
      },
      {
        name: 'solutions',
        label: 'Soluções'
      },
      {
        name: 'plans',
        label: 'Planos'
      },
      {
        name: 'differentials',
        label: 'Diferenciais'
      },
      {
        name: 'abount',
        label: 'Sobre nós'
      },
      {
        name: 'contact',
        label: 'Contato'
      },
      {
        name: 'fac',
        label: 'FAC'
      }
    ]
  })
}
</script>

<style lang="stylus">
@import 'styles.styl'
</style>
