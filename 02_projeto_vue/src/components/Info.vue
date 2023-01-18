<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes linguagens para front-end</p>
    <ul>
      <li v-for="(technology, index) in frontend_technologies" v-bind:key="index">{{ technology }}</li>
    </ul>
    <p>Utilizo as seguintes linguagens para back-end</p>
    <ul>
      <li v-for="technology in backend_technologies" :key="technology.id">
        {{ technology.language }}
      </li>
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
      texto_botao: "Mostrar Email",
      frontend_technologies: ['Javascript', 'Typescript', 'Vue'],
      backend_technologies: [
        { id: 1, language: 'Python' },
        { id: 2, language: 'C#' },
        { id: 3, language: 'Java' }
      ]
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