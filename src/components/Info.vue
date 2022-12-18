<template>
    <div> 
        <p>{{outraProp}}</p>
        <p>{{outraProp}} - {{propEmail}}</p>
        <p v-if="esta_trabalhando" > Ola  sou uma boa pessoa</p>
        <p v-else > Não sou uma boa pessoa</p>
        <p v-show="mostrar_email">{{email}}</p>

        <ul>
            <li v-for="(pessoa, index) in mexicanos" v-bind:key="index">{{pessoa}}</li>
        </ul>
        <ul>
            <li v-for="profissao in profissoes" v-bind:key="profissao.id">
                {{profissao.id}} - {{profissao.descricao}}
            </li>
        </ul>
        <p>Utilizo as seguintes tecnologias</p>
         
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
    props:{
        outraProp: String,
        propEmail: String
    },
    data() {
        return {esta_trabalhando: false, 
                mostrar_email: false, 
                email:'roberto@gmail.com', 
                meu_link:'https://goolge.com',
                texto_botao:"Mostar email",
                mexicanos:['MIGUEL','CARMEN','RAMON', 'LEON', 'MARCELA', 'DOLORES'],
                profissoes:[{id:1, descricao:"Tosador", funcao:"Cortar pelo de animais"},
                            {id:2, descricao:"Caixa", funcao:"Receber e valores consumido pelo cliente"},
                            {id:3, descricao:"Veterinario", funcao:"Tratar saúde do animal"}]
            }
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
