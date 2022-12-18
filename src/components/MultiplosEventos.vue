<template>
    <div>
        <button @click="primeiro(txt_evento_1,$event),
                        segundo(txt_evento_2,$event),
                        terceiro($event)">
            Multiplos eventos
        </button>
        <p>
            {{multiplos_eventos_1}}
        </p><p>
            {{multiplos_eventos_2}}
        </p>
    </div>
</template>

<script>

export default {
    name:"MultiplosEventos",
    data(){
        return{
            multiplos_eventos_1:"",
            multiplos_eventos_2:"",
            txt_evento_1:"Primeiro evento",
            txt_evento_2:"Segundo evento"
        }
    },
    methods:{
        primeiro(txt1, e){
            e.preventDefault();
            this.multiplos_eventos_1 =txt1;
        },

        segundo(txt2, e){
            e.preventDefault();
            setTimeout(()=>this.multiplos_eventos_2 = txt2, 3000);
        },

        terceiro(e){
            e.preventDefault();
            setTimeout(
                ()=>{
                    this.multiplos_eventos_1 = ""; 
                    this.multiplos_eventos_2 = "";
                }, 5000);
        }
    }
}
</script>

<style scoped>
div{
    margin: 30px;
}
</style>
