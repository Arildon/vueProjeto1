<template>
    <h2>*****************</h2>
    <h2>Login Pessoa Formulário Externo</h2>
        <!-- <form action="" @submit="enviarFormulario($event)"></form> -->
        <form action="" @submit="enviarFormulario">
            <div>
                <!-- <InputText @emitClick="getLink" @getChange="getChange"/> -->
                <InputText @getLogin="getLogin" @getSenha="getSenha"/>
            </div>
            <div>
                <SubmitButton />
            </div>
    </form>
    <div>
        <p>Um teste com o {{loginExterno}} e a {{senhaExterna}}</p>
    </div>
    <h2>Login Pessoa Formulário Interno</h2>
        <form action="" @submit="enviarFormularioInterno($event)">
            <div>
                <input type="text" placeholder="login" v-model="loginInterno">
            </div>
            <div>
                <input type="text" placeholder="senha" v-model="senhaInterna">
            </div>
            <div>
                <input type="submit" value="Enviar">
            </div>
        </form>
        <div>
            <p>Um teste com o {{loginInterno}} e a {{senhaInterna}}</p>
        </div>
</template>

<script>
import InputText from './form/InputText.vue'
import SubmitButton from './form/SubmitButton.vue'

export default {
    name: 'FormPessoa',
    components: {
        InputText,
        SubmitButton
    },

    data() {
        return {
            loginExterno: "",
            senhaExterna: "",
            loginInterno: "",
            senhaInterna: ""
        }
    },

    methods: {
        enviarFormulario(e) {
            e.preventDefault();
            console.log( this.loginExterno, this.senhaExterna)  
        },
            
        enviarFormularioInterno(e) {
            e.preventDefault()
            const loginInterno = this.loginInterno
            const senhaInterna = this.senhaInterna
            console.log(`O Email é ${loginInterno} e a senha é ${senhaInterna}`)
        },

        getLoginSenha (){
            console.log( this.loginExterno, this.loginExterno)
        },

        getLogin(value){
            this.loginExterno = value
        },

        getSenha(value){
            this.senhaExterna = value
        }
    }
}
</script>