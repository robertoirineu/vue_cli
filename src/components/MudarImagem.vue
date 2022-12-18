<template>
    <button @click="$emit('trocarImagem')"> Trocar imagem </button>
</template>

<script>
export default {
   name:"MudarImagem",
   emits:["trocarImagem"]
}
</script>
