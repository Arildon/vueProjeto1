<template>
    <div>
        <button @click="ativar">Clique aqui fedazunha!</button>
        <span v-show="clicou">Clicou mesmo hein!?</span>
    </div>
</template>

<script>
export default {
    name: 'ReutilizacaoComponente',
    data() {
        return {
            clicou: false
        }
    },
    methods: {
        ativar() {
            this.clicou = !this.clicou
        }
    }
}
</script>

<style scoped>

</style>