<template>
  <span>
    <div class="card-image" v-if="img">
      <img :src="img">
      <span class="card-title">{{titulo || ''}}</span>
    </div>

    <div class="card-content" v-if="texto">
      <p>{{texto}}</p>
    </div>
  </span>
</template>

<script>

export default {
    name: 'CardDetalheVue',
    props:['img','titulo','texto'],
    data () {
        return {

        }
    }
}
</script>