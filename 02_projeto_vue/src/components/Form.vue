<template>
  <form action="" @submit="enviarFormulario">
    <div>
      <input type="text" v-model="name" placeholder="Nome">
    </div>
    <div>
      <input type="text" v-model="email" placeholder="E-Mail">
    </div>
    <div>
      <Submit />
    </div>
  </form>
  <p>Conteudo</p>
  <p>Conteudo</p>
  <p>Conteudo</p>
</template>

<script>
import InputText from "./form/InputText.vue";
import Submit from "./form/Submit.vue";
export default {
  name: "Form",
  components: {
    InputText,
    Submit,
  },
  data() {
    return {
      name: "",
      email: ""
    }
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

      console.log("formulario enviado")
      console.log("O Nome é: " + name)
      console.log("O E-Mail é: " + email)

      //Ajax

      //Inserir dados no banco
    }
  }
}
</script>

<style scoped>
p {
  margin: 150px;
}
</style>