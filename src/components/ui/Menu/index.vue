<template>
  <nav class="menu">
    <a
      @click="setActiveOption(option.name)"
      :ref="option.name"
      :href="option.link"
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
    },
    applyScrool (name) {
      let scrool = 0
      const defaultSize = 748

      switch (name) {
        case 'home':
          scrool = 0
          break
        case 'solutions':
          scrool = defaultSize
          break
        case 'plans':
          scrool = defaultSize * 2
          break
        case 'differentials':
          scrool = defaultSize * 3
          break
        case 'abount':
          scrool = defaultSize * 4
          break
        case 'contact':
          scrool = defaultSize * 5
          break
        case 'fac':
          scrool = defaultSize * 6
          break
      }

      window.scroll(0, scrool)
    }
  },
  watch: {
    active (newValue, oldValue) {
      this.$refs[newValue][0].classList.add('a-visited')

      if (oldValue) {
        this.applyScrool(newValue)

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
        label: 'Home',
        link: '#home'
      },
      {
        name: 'solutions',
        label: 'Soluções',
        link: '#solucoes'
      },
      {
        name: 'plans',
        label: 'Planos',
        link: '#planos'
      },
      {
        name: 'differentials',
        label: 'Diferenciais',
        link: '#diferenciais'
      },
      {
        name: 'abount',
        label: 'Sobre nós',
        link: '#sbre'
      },
      {
        name: 'contact',
        label: 'Contato',
        link: '#contato'
      },
      {
        name: 'fac',
        label: 'FAC',
        link: '#fac'
      }
    ]
  })
}
</script>

<style lang="stylus">
@import 'styles.styl'
</style>
