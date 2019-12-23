<template>
    <span>

        <header>
            <navbar-vue cor="indigo darken-4" logo="Social" url="/">
                <li><router-link to="/">Home</router-link></li>
                <li><router-link to="/login">Entrar</router-link></li>
            </navbar-vue>
        </header>

        <main>
            <div class="container">
                <div class="row">
                    <grid-vue col="6">
                        <slot name="left" />
                    </grid-vue>
                    <grid-vue col="4 offset-s1">
                        <slot name="right" />
                    </grid-vue>
                </div>
            </div>
        </main>
    </span>
</template>

<script>
import NavbarVue from '@/components/layouts/NavbarVue'
import GridVue from '@/components/layouts/GridVue'
export default {
    name: 'TemplateLogin',
    components: {
        NavbarVue,
        GridVue
    }
}
</script>