<template>
    <div>
        <img v-if="btnTrocaImagem" :src="imagemArildon" :alt="descricao">
        <!-- Usando o : é o mesmo que o V-Bind, só que de forma simplificada -->
    </div>
    <div>
        <TrocarImagem @trocar-imagem="trocarimagem"/>
    </div>
</template>

<script>
import TrocarImagem from './TrocarImagem.vue'

export default {
    name: 'PicturePessoa',

    components: {
        TrocarImagem
    },

    data() {
        return {
            imagemArildon: '/img/Ari02.png',
            // usando o / é um atalho para a pasta public como o exemplo /img é public/img
            descricao: 'Arildon Ferraz',
            btnTrocaImagem: true
        }
    },
    
    methods: {
        trocarimagem() {
            this.trocarImagem =! this.trocarImagem
            if (this.trocarImagem) {
                this.imagemArildon = '/img/Ari01.png'            
            }
            else {
                this.imagemArildon = '/img/Ari02.png' 
            }
            
        }
    }
}
</script>

<style scoped>
img{
    max-height: 200px;
}
</style>