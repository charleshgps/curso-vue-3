<template>
  <div>
    <h1>Meu nome é: {{ nome }}</h1>
  </div>
</template>

<script>
export default {
  name: "LifeCycle",
  data() {
    return {
      nome: "Charles",
    };
  },
  created() {
    setTimeout(() => {
      this.nome = "Chagg";
    }, 1000);
    this.lifeCycle()
  },
  mounted() {
    setTimeout(() => {
      this.nome = "Chaggnorris";
    }, 2000);
    this.lifeCycle()
  },
  methods: {
    lifeCycle() {
      console.log('Executou')
    }
  }
};
</script>

