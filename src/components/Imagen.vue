<template>
    <img :src="avatar" :alt="descricao" />
</template>
<script>

export default {
    name:"Imagen",
    data(){
        return{
            avatar: "/img/logo.png",
            descricao: "imagem do avatar"
        }
        
    }
}
</script>
