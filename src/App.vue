<template>
  <PrimeiroComponente />
  <CicloDeVida />
  <Pessoa />
  <Form/>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import CicloDeVida from './components/CicloDeVida.vue';
import Pessoa from './components/Pessoa.vue';
import Form from './components/Form.vue';

export default {
  name: 'App',
  components:{
    Form,
    PrimeiroComponente,
    CicloDeVida,
    Pessoa
  }
}
</script>