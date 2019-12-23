<template>

    <template-login>

        <section slot="left">
            <p class="center-align">
                <img src="https://www.startupsstars.com/wp-content/uploads/2016/02/gerenciamento-social.png" class="responsive-img" />    
            </p>            
        </section>
        <section slot="right">
            <h2 class="center-align blue-text text-darken-2">Login</h2>
            <div class="row">
                <form>
                    <div class="row">
                        <div class="input-field">
                            <input id="email" type="email" class="validate">
                            <label for="email">Email</label>
                            <span class="helper-text" data-error="wrong" data-success="right" v-if="error_email">Helper text</span>
                        </div>
                        <div class="input-field">
                            <input id="senha" type="password" class="validate">
                            <label for="senha">Senha</label>
                            <span class="helper-text" data-error="wrong" data-success="right" v-if="error_senha">Helper text</span>
                        </div>
                        <input type="submit" value="Entrar" class="waves-effect waves-light btn" />
                        <router-link to="/register" class="btn waves-effect waves-light">Registre-se</router-link>
                    </div>
                </form>
            </div>
        </section>
    </template-login>
</template>

<script>
import TemplateLogin from '@/templates/TemplateLogin'
import GridVue from '@/components/layouts/GridVue'

export default {
    name: 'Login',
    data () {
        return {
            error_email: false,
            error_senha: false
        }
    },
    components: {
        TemplateLogin,
        GridVue
    }
}
</script>