<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes linguagens</p>
    <ul>
      <li>Javascript</li>
      <li>Typescript</li>
      <li>Vue</li>
    </ul>
    <div>
      <button @click="showEmail">{{ texto_botao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p>
      Para acessar o meu portifólio
      <a v-bind:href="meu_link">Basta clicar aqui</a>
    </p>
    <Picture />
  </div>
</template>

<script>
import Picture from "./Picture";
export default {
  name: "info",
  components: {
    Picture,
  },
  data() {
    return {
      esta_trabalhando: true,
      mostrar_email: false,
      email: "charles_humberto@hotmail.com.br",
      meu_link: "https://portfolio-charles-silva.netlify.app/",
      texto_botao: "Mostrar Email"
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
      if (!this.mostrar_email) {
        this.texto_botao = "Mostrar Email"
      } else {
        this.texto_botao = "Esconder Email"
      }
    }
  }
};
</script>