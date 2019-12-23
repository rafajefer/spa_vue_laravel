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
                    <grid-vue col="4">
                        <slot name="left" />
                    </grid-vue>
                    <grid-vue col="8">
                        <slot name="right" />
                    </grid-vue>
                </div>
            </div>
        </main>
        <footer-vue cor="indigo darken-4" logo="Social" descricao="Teste de descrição" ano="2019">
            <li><a class="grey-text text-lighten-3" href="#!">Home</a></li>
            <li><a class="grey-text text-lighten-3" href="#!">Link 2</a></li>
            <li><a class="grey-text text-lighten-3" href="#!">Link 3</a></li>
            <li><a class="grey-text text-lighten-3" href="#!">Link 4</a></li>
        </footer-vue>
    </span>
</template>

<script>
import NavbarVue from '@/components/layouts/NavbarVue'
import FooterVue from '@/components/layouts/FooterVue'
import GridVue from '@/components/layouts/GridVue'

export default {
    name: 'TemplateSite',
    components: {
        NavbarVue,
        FooterVue,
        GridVue
        // CardVue
    }
}
</script>