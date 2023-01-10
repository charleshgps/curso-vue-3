<template>
  <div>
    <FirstComponent />
    <LifeCycle/>
  </div>
</template>

<script>
import FirstComponent from "./components/FirstComponent.vue";
import LifeCycle from "./components/LifeCycle.vue";

export default {
  name: "App",
  components: {
    FirstComponent,
    LifeCycle,
  },
};
</script>