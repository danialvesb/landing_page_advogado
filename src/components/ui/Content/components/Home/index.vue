<template>
  <div class="home">
    <div class="information">
      <h1>{{ text_1 }}</h1>
      <h4>{{ text_02 }}</h4>
      <button-ui value="Fale com a gente"/>
    </div>
    <div class="banner" />

  </div>
</template>

<script>
import ButtonUi from '@/components/form/Button'
export default {
  name: 'home-content',
  components: {
    ButtonUi
  },
  data: () => ({
    text_1: 'Plataforma de marketing direto mais completa do mercado',
    text_02: 'A Marketing Trends facilita o envio de mensagens customizadas para divulgação no WhatsApp e SMS, além da construção de um mailing qualificado que gera oportunidades de negócios reais!'
  })
}
</script>

<style lang="stylus" scoped>
@import 'styles.styl'
</style>
