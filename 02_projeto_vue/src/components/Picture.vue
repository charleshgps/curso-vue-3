<template>
  <img :src="avatar" :alt="descricao" />
  <MudarImg @mudar-img="alterarImg"/>
</template>

<script>
import MudarImg from './MudarImg.vue'

export default {
  name: "Picture",
  components:{
    MudarImg
  },
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "Charles Humberto",
    };
  },
  methods:{
    alterarImg(){
      this.avatar = "/img/avatar2.png"
    }      
  }
};
</script>
