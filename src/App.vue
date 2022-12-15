<template>

  <Header/>
  <p class="stilo_pai">O dado do app é {{dado}} </p>
  <PrimeiroComponente />
  <CicloDeVida />
  <Pessoa />
  <Form/>
</template>

<script>

import Header from './components/Header.vue';
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import CicloDeVida from './components/CicloDeVida.vue';
import Pessoa from './components/Pessoa.vue';
import Form from './components/Form.vue';

export default {
  name: 'App',
  components:{
    Header,
    Form,
    PrimeiroComponente,
    CicloDeVida,
    Pessoa
  },
  data(){
    return{
      dado:'Isso é um dado'
    }
  }
}
</script>
<style>
  body{
    background: #333;
    color: #fff;  
  }
  a{
    color: red;
  }
  .teste{
    background:#000;
  }
</style>