<template>

  <template-site>
    
    <section slot="left">
      <card-vue>
          <div class="row valign-wrapper">
              <grid-vue col="4">
                <img src="https://materializecss.com/images/yuna.jpg" alt="" class="circle responsive-img"> 
              </grid-vue>
              <grid-vue col="8">
                <span class="black-text">
                  <h5>Maria Silva</h5>
                  Add the "circle" class to it to make it appear circular.
                </span>
              </grid-vue>
          </div>
      </card-vue>
    </section>

    <section slot="right">
      <publicar-vue />
      <card-conteudo-vue photo="https://materializecss.com/images/yuna.jpg" nome="Maria Silva" data="12/01/19 12:30">
        <card-detalhe-vue 
          img="https://materializecss.com/images/sample-1.jpg" 
          texto="I am a very simple card. I am good at containing small bits of information. I am convenient because I require little markup to use effectively." />
      </card-conteudo-vue>
    </section>

    

  </template-site>

  
  
</template>

<script>
import TemplateSite from '@/templates/TemplateSite'
import CardConteudoVue from '@/components/social/CardConteudoVue'
import CardDetalheVue from '@/components/social/CardDetalheVue'
import PublicarVue from '@/components/social/PublicarVue'
import CardVue from '@/components/layouts/CardVue'
import GridVue from '@/components/layouts/GridVue'

export default {
  name: 'Home',
  data () {
    return {
        
    }
  },
  components: {
    TemplateSite,
    CardConteudoVue,
    CardDetalheVue,
    PublicarVue,
    CardVue,
    GridVue
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
