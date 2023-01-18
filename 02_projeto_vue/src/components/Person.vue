<template>
  <div>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <Info :email="email" :esta_trabalhando="false" />
    <Form />
  </div>
</template>

<script>
import Info from "./Info";
import Form from "./Form";
export default {
  components: { Info },
  name: "Person",
  components: {
    Info,
    Form,
  },
  data() {
    return {
      nome: "Charles",
      email: "Charles_humberto@hotmail.com.br"
    };
  },
};
</script>