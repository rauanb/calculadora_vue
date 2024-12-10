<script setup>
  import Header from './components/Header.vue';
  import Footer from './components/Footer.vue';
  import Form from './components/Form.vue';
  import Return from './components/Return.vue';
  
import { reactive } from 'vue';

  const estado = reactive({
    operador1: 1,
    operador2: 1,
    operacao: 'Soma',
    resposta: 2
  })

  function mostraOperador1() {
    return estado.operador1
  }

  function mostraOperador2() {
    return estado.operador2
  }

  function mostraOperacao() {
    // return estado.operacao
    const { operacao } = estado;

    switch (operacao) {
      case 'Soma':
        estado.resposta = estado.operador1 + estado.operador2;
        return '+';
      case 'Subtracao':
        estado.resposta = estado.operador1 - estado.operador2;
        return '-';
      case 'Multiplicacao':
        estado.resposta = estado.operador1 * estado.operador2;
        return '*';
      case 'Divisao':
        estado.resposta = estado.operador1 / estado.operador2;
        return '/'
    }
  }
  
  function mostraResposta() {
    if (estado.operacao == 'Divisao' && estado.operador2 === 0) {
        return "Indefinido"
    } else {
      return estado.resposta
    }
  }
</script>

<template>
  <div class="container">
    <Header />
    
    <Form 
    :altera-operacao="evento => estado.operacao = evento.target.value"
    :altera-operador1="evento => estado.operador1 = parseInt(evento.target.value)"
    :altera-operador2="evento => estado.operador2 = parseInt(evento.target.value)"
    />
    
    <Return 
    :mostra-operador1="mostraOperador1()"
    :mostra-operador2="mostraOperador2()"
    :mostra-operacao="mostraOperacao()"
    :mostra-resposta="mostraResposta()" 
    />

    <Footer  />
  </div>
</template>

<style scoped>
  /* .container {
    max-width: 60%;
    margin: 0 auto;
    text-align: center
  } */
</style>
