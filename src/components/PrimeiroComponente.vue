<template>
    <div>
        <h1>Olá Vue...!!!!</h1><br />
        Meu nome é: {{nome}}<br />
        Sobrenome: {{sobrenome}}
    </div>    
</template>

<script>
import { createDOMCompilerError } from '@vue/compiler-dom';

export default {
    name: "PrimeiroComponente",
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
        }, 3000)      
        
    },

    //Executa depois do create()
    mount(){
        setTimeout(()=>{
        this.nome = 'Alberto'
        }, 5000)
    }
}
</script>
