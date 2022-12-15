<template>
    <div>
        <p v-if="esta_trabalhando" > Ola  sou uma boa pessoa</p>
        <p v-else > Não sou uma boa pessoa</p>
        <p v-show="mostrar_email">{{email}}</p>
    </div>

</template>

<script>

export default {
    name:'Info',
    data() {
        return {esta_trabalhando: false, mostrar_email: true, email:'roberto@gmail.com'}
    },
}
</script>
