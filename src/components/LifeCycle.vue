<template>
    <h2>Meu Nome é: {{nome}}</h2>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: 'Ainda não sei'
        }
    },
    created() {
        setTimeout(() => {
            this.nome = 'Arildon'
        }, 3000);
        this.lifeCycle()
    },
    mounted() {
        setTimeout(() => {
            this.nome = 'Ferraz'
        }, 3000);
        this.lifeCycle()
    }, 
    methods: {
        lifeCycle() {
            console.log('Executou o LifeCycle')
        }
    }
}
</script>