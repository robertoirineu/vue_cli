<template>
    <div>
        <form action="">
            <div><input-text /></div>
            <div><input-text /></div>
            <div><submit /></div>                
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
    }
}
</script>
