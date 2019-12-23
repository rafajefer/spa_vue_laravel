<template>
    <template-login>
        <section slot="left">
            <img src="https://www.startupsstars.com/wp-content/uploads/2016/02/gerenciamento-social.png" class="center-align responsive-img" />    
        </section>
        <section slot="right">
            <h2 class="center-align blue-text text-darken-2">Registra-se</h2>
            <div class="row">
                <form>
                    <div class="row">
                        <div class="input-field">
                            <input id="nome" type="text" class="validate">
                            <label for="nome">Nome</label>
                        </div>
                        <div class="input-field">
                            <input id="email" type="email" class="validate">
                            <label for="email">Email</label>
                        </div>
                        <div class="input-field">
                            <input id="senha" type="password" class="validate">
                            <label for="senha">Senha</label>
                        </div>
                        <div class="input-field">
                            <input id="confSenha" type="password" class="validate">
                            <label for="confSenha">Confirme sua Senha</label>
                        </div>
                        <input type="submit" value="Enviar" class="waves-effect waves-light btn" />
                        <router-link to="/login" class="btn waves-effect waves-light orange">Já tenho cadastro</router-link>
                    </div>
                </form>

            </div>
        </section>
    </template-login>
</template>

<script>
import TemplateLogin from '@/templates/TemplateLogin'
export default {
    name: 'Register',
    data () {
        return {

        }
    },
    components: {
        TemplateLogin
    }
}
</script>