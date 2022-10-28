<template>
  <div>
    <!-- <input type="text"> -->
    <input placeholder="Login" v-model.trim="login" v-on:keyup="getLogin($event.target.value)" />
  </div>
  <div>
    <input placeholder="Senha" v-model.trim="senha" v-on:keyup="getSenha($event.target.value)"/>
  </div>
  <!-- <button @click = "$emit('getLoginSenha')" >dafdafafd</button> -->
</template>

<script>

export default {
  name: "InputText",

  emits: ["getSenha", "getLogin"],

  data() {
    return {
      login: "", 
      senha: ""
    }
  },

  methods: {
    // emitClick(){
    //   this.$emit('emitClick', this.login, this.senha)
    // },
    getSenha(value){
      this.$emit('getSenha', value)
    },
    getLogin(value) {
      this.$emit('getLogin', value)
    }
  }
}
</script>
