
<template>
  <HeaderSite :esta_logado="esta_logado"/>
  <PrimeiroComponente />
  <h4>Assunto: {{retorno}}</h4>
  <LifeCycle />
  <ExemploPessoa />
</template>

<script>
  import HeaderSite from './components/HeaderSite.vue'
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from  './components/LifeCycle.vue'
  import ExemploPessoa from './components/ExemploPessoa.vue'

  export default {
    name: 'App',
    components: {
    HeaderSite,
    PrimeiroComponente,
    LifeCycle,
    ExemploPessoa,
},
    data() {
      return {
        esta_logado: true,
        retorno : 'Aprendendo Vue'
      }
    }
  }
</script>

<style>
  body {
    background-color: #fcfcfc;
    color: #3c474b;
    margin: 10px;
    font-family: Arial, Helvetica, sans-serif;
  }

  a {
    color: #c72727
  }

  h1 {
    color: black;
    font-family: Tahoma;
    text-align: center;
    text-decoration: underline;
  }
</style>