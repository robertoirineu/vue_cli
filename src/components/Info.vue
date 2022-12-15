<template>
    <div>
        <p v-if="esta_trabalhando" > Ola  sou uma boa pessoa</p>
        <p v-else > Não sou uma boa pessoa</p>
        <p v-show="mostrar_email">{{email}}</p>

        <div>
            <button @click="showEmail">{{texto_botao}}</button>
        </div>
        <p class="teste"> Para acessar meu histórico 
            <a v-bind:href="meu_link" target="_blank" >basta clicar aqui</a>
        </p>
        <Imagem/>
    </div>

</template>

<script>
import Imagem from "./Imagen.vue"

export default {
    name:'Info',
    components:{
        Imagem
    },
    data() {
        return {esta_trabalhando: false, 
                mostrar_email: false, 
                email:'roberto@gmail.com', 
                meu_link:'https://goolge.com',
                texto_botao:"Mostar email"}
    },
    methods:{
        showEmail(){
            this.mostrar_email = !this.mostrar_email;
            if(!this.mostrar_email){
                this.texto_botao = "Mostrar e-mail"

            }else{
                this.texto_botao = "Ocultar e-mail"
            }
        }
    }
}
</script>

<style>
.stilo_pai{
    color: blue;
}
</style>
