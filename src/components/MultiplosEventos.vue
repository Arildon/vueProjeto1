<template>
    <div>
        <button @click="primeiroMetodo(txt1, $event), segundoMetodo(txt2, $event), terceiroMetodo($event)">Ativar múltiplos eventos</button>
        <p>{{multiplos_eventos}}</p>
    </div>
</template> 

<script>
    export default{
        name: 'MultiplosEventos',
        data() {
            return {
                multiplos_eventos: "",
                txt1: "Primeiro Evento",
                txt2: "Segundo Evento",
            }
        },
        methods: {
            primeiroMetodo(txt) {
                this.multiplos_eventos = txt
            },
            segundoMetodo(txt) {
                setTimeout(() => this.multiplos_eventos = txt, 1500)
            },
            terceiroMetodo() {
                setTimeout(() => this.multiplos_eventos = "", 1500)
            }
        }
    }
</script>

<style scoped>
    div {
        margin: 50px;
    }

    button {
        background-color: #000;
        color: #FFF
    }

    button:hover {
        background-color: rgb(136, 42, 42);
        color: #FFF
    }
</style>