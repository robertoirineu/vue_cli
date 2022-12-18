<template>
    <div>
        <form action="" @submit="enviarFormulario($event)">
            <div>
                <input type="text" v-model='nome' />
            </div>
            <div>
                <input type="text" v-model='email' />
            </div>
            <div>
                <submit />
            </div>                
        </form>        
    </div>    
</template>

<script>
import InputText from './form/inputText.vue'
import Submit from './form/Submit.vue'

export default {
    name:'Form',
    components:{
        InputText,
        Submit
    },
    data(){
        return{
            nome:"f",
            email:"e"
        }
    },
    
    methods:{
        enviarFormulario(e){
            e.preventDefault();

            const nme = this.nome;
            const mail = this.email;

            console.log("Evento");
            console.log(nme);
            console.log(mail);
        }
    }
}
</script>
