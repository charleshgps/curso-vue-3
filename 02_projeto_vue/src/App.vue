<template>
  <div>
    <FirstComponent />
    <LifeCycle/>
    <Person/>
  </div>
</template>

<script>
import FirstComponent from "./components/FirstComponent.vue";
import LifeCycle from "./components/LifeCycle.vue";
import Person from './components/Person.vue';

export default {
  name: "App",
  components: {
    FirstComponent,
    LifeCycle,
    Person,
  },
};
</script>