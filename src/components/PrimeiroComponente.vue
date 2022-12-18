<template>
    <div>
        <h1>Olá Vue...!!!!</h1><br />
        Meu nome é: {{nome}}<br />
        Sobrenome: {{sobrenome}}
        <MultiplosEventos/>
        <Reutilizacao/>
    </div>    
</template>

<script>

import MultiplosEventos from "./MultiplosEventos.vue" 
import Reutilizacao from "./Reutilizacao.vue" 

export default {
    name: "PrimeiroComponente",
    components:{
        MultiplosEventos,
        Reutilizacao
    },
    data(){
        return{
            nome:"Roberto",
            sobrenome: "Floro"
        }
    },

    //Executa apos a criacao da pagina depois do data()
    created(){
        setTimeout(()=>{
            this.nome='ola'
        }, 10000)      
        this.ciclodevida()        
    },

    //Executa depois do create()
    mounted(){
        setTimeout(()=>{
        this.nome = 'Alberto'
        }, 15000)
        this.ciclodevida()
    },

    methods:{
        ciclodevida(){
            console.log("EXECUTOU");
        }        
    }
}
</script>
