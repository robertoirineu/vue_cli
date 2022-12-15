<template>
<h2>Essa é a descrição da pessoa: {{nome}}</h2>
<Info />
</template>

<script>
    import Info from './Info'
    export default{
        name:'',
        components:{
            Info
        },        
        data(){
            return{
                nome:'Taniel'
            }
        }        
    } 
</script>