<template>

    <div class="row">
      <div class="card">
          <div class="card-content">
            <div class="row valign-wrapper">
              <grid-vue col="1">
                <img :src="photo" :alt="nome" class="circle responsive-img"> <!-- notice the "circle" class -->
              </grid-vue>
              <grid-vue col="11">
                <span class="black-text">
                  <strong>{{nome}}</strong> - <small>{{data}}</small>
                  
                </span>
              </grid-vue>
            </div>
            <slot />
          </div>
          <div class="card-action">
          <p>
              <i class="material-icons">favorite_border</i>
              <i class="material-icons">insert_comment</i>
          </p>
          </div>
      </div>
    </div>
</template>

<script>
import GridVue from '@/components/layouts/GridVue'

export default {
    name: 'CardConteudoVue',
    props:['photo','nome','data'],
    data () {
        return {

        }
    },
    components: {
      GridVue
    }
}
</script>