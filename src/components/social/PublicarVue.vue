<template>
    <div class="row">
      <grid-vue class="input-field" col="12">
        <textarea id="conteudo" class="materialize-textarea" v-model="conteudo"></textarea>
        <label for="conteudo">O que está acontencendo?</label>
      </grid-vue><br />
      <grid-vue class="btn waves-effect waves-light" col="2 offset-s10" v-if="conteudo">Publicar</grid-vue>
    </div>
</template>

<script>
import GridVue from '@/components/layouts/GridVue'

export default {
    name: 'PublicarVue',
    props:[],
    data () {
        return {
            conteudo: ''
        }
    },
    components:{
        GridVue
    }    
}
</script>