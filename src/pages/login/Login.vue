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
                        <router-link to="/register" class="btn waves-effect waves-light orange">Registre-se</router-link><br /><br />
                        <a href="#" v-on:click="recupera_senha = !recupera_senha">Esqueci minha senha</a><br />

                        <div class="input-field" v-if="recupera_senha">
                            <input id="recupera_senha" type="email" class="validate">
                            <label for="recupera_senha">Digite seu email</label>
                            <i class="material-icons prefix">send</i>
                            <span class="helper-text" data-error="wrong" data-success="right" v-if="message">Nova senha enviado com sucesso para ....</span>
                        </div>
                    </div>
                </form>
            </div>
        </section>
    </template-login>
</template>

<script>
import TemplateLogin from '@/templates/TemplateLogin'

export default {
    name: 'Login',
    data () {
        return {
            error_email: false,
            error_senha: false,
            message: false,
            recupera_senha: false
        }
    },
    components: {
        TemplateLogin
    }
}
</script>

<style scoped>
 /* label color */
   .input-field label {
     color: #000;
   }
   /* label focus color */
   .input-field input[type=text]:focus + label {
     color: #000;
   }
   /* label underline focus color */
   .input-field input[type=text]:focus {
     border-bottom: 1px solid #000;
     box-shadow: 0 1px 0 0 #000;
   }
   /* valid color */
   .input-field input[type=text].valid {
     border-bottom: 1px solid #000;
     box-shadow: 0 1px 0 0 #000;
   }
   /* invalid color */
   .input-field input[type=text].invalid {
     border-bottom: 1px solid #000;
     box-shadow: 0 1px 0 0 #000;
   }
   /* icon prefix focus color */
   .input-field .prefix.active {
     color: #000;
   }
     
</style>