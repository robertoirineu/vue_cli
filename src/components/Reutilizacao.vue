<template>
    <div>
        <button @click="ativar" >Cliaque aqui</button><br />
        <span v-show="ativou">Ativado!</span>
    </div>
</template>

<script>

export default{
    name:"Reutilizacao",
    data(){
        return{ativou:false}
    },
    methods: {
        ativar(){
            this.ativou = !this.ativou;
        }
    }
}
</script>
