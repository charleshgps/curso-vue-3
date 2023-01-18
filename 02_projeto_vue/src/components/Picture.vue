<template>
  <img :src="avatar" :alt="descricao" />
</template>
<script>
export default {
  name: Picture,
  data() {
    return {
      avatar: "/img/avata.png",
      descricao: "Charles Humberto",
    };
  },
};
</script>