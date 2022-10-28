<template>
    <div>
        <p><input type="checkbox" id="checkbox" @click="showEmail"> Mostrar E-mail</p>
        <button @click="showEmail">{{texto_botao}}</button>
        <text v-show="mostrar_email"><b>Usuário Logado com o Email <u>{{email}}</u></b></text>
    </div>
    <p>{{email}} veio do Data deste componente (InfoPessoa)</p>
    <p>{{pessoaEmail2}} Veio do componente pai (ExemploPessoa) hardcoded</p>
    <p>{{pessoaEmail3}} é outra forma de passar o valor para outro componente via data do pai</p>
    <p v-if="esta_trabalhando">Estou trabalahando no momento.</p>
    <p v-else>Estou em busca de Emprego</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <!-- <ul>
        <li>C#</li>
        <li>JavaScript</li>
        <li>SQL</li>
    </ul> -->
    <ul>
        <li v-for="(tecnologia, index) in tecnologias_trabalho" v-bind:key="index">{{tecnologia}}</li>
    </ul>
    <p>Não trabalho com as tecnologias</p>
    <ul>
        <li v-for="tecnologia in tecnologias_naotrabalho" :key="tecnologia.id">{{tecnologia.tecnologia}}</li>
        <!-- os : é a uma abreviação para v-bind: -->
    </ul>
    <p>Para acessar o meu Currículo, <a v-bind:href="meu_link" target="_blank">clique aqui</a></p>    
    <PicturePessoa />    
</template>

<script>
import PicturePessoa from './PicturePessoa.vue'

export default {
    name: 'InfoPessoa',
    components: {
        PicturePessoa
    },
    props: {
        pessoaEmail2: String,
        pessoaEmail3: String
        // se for array, não precisa determinar o tipo. Ex: props: ["esta_logado"]
    },
    data() {
        return {
            email: 'arildonfneves@hotmail.com',
            esta_trabalhando: true,
            mostrar_email: false,
            meu_link: 'https://google.com',
            texto_botao: 'Mostrar E-mail',
            tecnologias_trabalho: ['C#','JavaScript','SQL'],
            tecnologias_naotrabalho: [
                {id: 1, tecnologia: 'C++'},
                {id: 2, tecnologia: 'Phyton'},
                {id: 3, tecnologia: 'Java'},
            ]
        }
    },
    methods: {
        showEmail() {
            // const checkbox = document.getElementById("checkbox")
            const checkbox = document.querySelector("#checkbox")
            this.mostrar_email = !this.mostrar_email
            if(this.mostrar_email) {
                this.texto_botao = 'Ocultar E-mail'
                checkbox.checked =true
            }
            else {
                this.texto_botao = 'Mostrar Email'
                checkbox.checked =false
            }
        }
    }
}
</script>