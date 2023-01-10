<template>
  <div>
    <h1>Ola Vue!!</h1>
    <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
  </div>
</template>

<script>
export default {
  name: "FirstComponent",
  data() {
    return {
      nome: "Charles",
      profissao: "Programador",
    };
  },
};
</script>