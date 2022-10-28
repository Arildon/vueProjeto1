<template>
    <p>______________________________________________</p>
    <h3>Este é um exemplo de descrição do {{nome}}</h3>
    <InfoPessoa pessoaEmail2="arildonfneves@email2.com" :pessoaEmail3="pessoaEmail3" />
    <FormPessoa />
</template>

<script>
import InfoPessoa from './InfoPessoa.vue';
import FormPessoa from './FormPessoa.vue';
export default {
    nane: 'ExemploPessoa',
    data() {
        return {
            nome: 'Arildon',
            pessoaEmail3: 'arildonfneves@email3.com'         
        };
    },
    components: { InfoPessoa, FormPessoa }
}
</script>