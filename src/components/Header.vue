<template>
    <ul>
        <li><a>Home</a></li>
        <li><a>Projetos</a></li>
        <li><a>Contato</a></li>
    </ul>
    
</template>
<script>

export default{
    name:"Header",
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
