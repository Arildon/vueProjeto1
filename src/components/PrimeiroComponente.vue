<template>
  <div>
    <h1>Site do Arildon</h1>
    <p>Meu nome é {{nome}}, sou {{profissao}} na empresa {{empresa}}.</p>
    <MultiplosEventos />
    <ReutilizacaoComponente />
    <ReutilizacaoComponente />
  </div>

</template>

<script>
  import MultiplosEventos from './MultiplosEventos.vue'
  import ReutilizacaoComponente from './ReutilizacaoComponente.vue'

  export default {
    name: 'PrimeiroComponente',
    components: {
      MultiplosEventos,
      ReutilizacaoComponente
    },
    data() {
      return {
        nome: 'Arildon',
        profissao: 'Analista de Sistemas',
        empresa: 'Valid',
      }
    }
  }
</script>