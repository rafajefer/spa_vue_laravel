<template>
    <div :class="'col s' + col">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: 'GridVue',
    props:['col'],
    data () {
        return {

        }
    }
}
</script>