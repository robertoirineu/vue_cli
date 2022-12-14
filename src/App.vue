<template>
  <PrimeiroComponente />
  <CicloDeVida />
  <Pessoa />
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import CicloDeVida from './components/CicloDeVida.vue';
import Pessoa from './components/Pessoa.vue'

export default {
  name: 'App',
  components:{
    PrimeiroComponente,
    CicloDeVida,
    Pessoa
  }
}
</script>