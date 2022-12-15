<template>
    <div>
        <h1>ROBERTO FLORO IRINEU DA SILVA</h1>
        {{nome}}
    </div>    
</template>
<script>

export default{
    name:  'CicloDeVida',
    data(){
        return{
            nome:'ola'
        }
    },

    create(){
        this.ciclodevida();
    },

    mouted(){
        this.ciclodevida();
    },

    methods:{
        ciclodevida(){
            console.log("EXECUTOU");
        }        
    }
}
</script>
