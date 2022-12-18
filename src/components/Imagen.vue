<template>
    <img :src="avatar" :alt="descricao" />
    <MudarImagem @trocarImagem="trocarImagem"/>
</template>
<script>
import MudarImagem from './MudarImagem.vue' 
export default {
    name:"Imagen",
    components:{
        MudarImagem
    },
    data(){
        return{
            avatar: "/img/logo.png",
            descricao: "imagem do avatar"
        }       
    }, 
    methods:{
        trocarImagem(){
            this.avatar="/img/Ampulheta.png";
        }
    }
}
</script>
