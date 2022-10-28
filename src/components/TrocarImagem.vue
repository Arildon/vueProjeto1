<template>
    <button @click="$emit('trocarImagem')">Trocar Imagem do Perfil</button>
</template>

<script>
export default {
    name: 'TrocarImagem',

    emits: ['trocarImagem'],
    
    data() {
        return {

        }
    }
}
</script>