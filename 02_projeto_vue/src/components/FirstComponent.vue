<template>
  <div>
    <h1>Ola Vue!!</h1>
    <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
    <MultriplosEventos />
    <Reutilizacao />
  </div>
</template>

<script>
import MultriplosEventos from './MultriplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue';

export default {
  name: "FirstComponent",
  components: {
    MultriplosEventos,
    Reutilizacao
  },
  data() {
    return {
      nome: "Charles",
      profissao: "Programador",
    };
  },
};
</script>