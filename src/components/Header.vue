<template>
    <ul>
        <li><a>Home</a></li>
        <li><a>Projetos</a></li>
        <li><a>Contato</a></li>
        <li v-if="estaLogado"><a>Meu perfil</a></li>
    </ul>
    
</template>
<script>

export default{
    name:"Header",
    props:["estaLogado"]
}
</script>
<style scoped>
    ul{
        list-style:none;
        display: flex;
    }
    li{
        margin-right: 10px;
    }
    a{
        color:#ddd;
        text-decoration: none;
    }
    a:hover{
        color: turquoise;
        cursor: pointer;
    }
</style>
