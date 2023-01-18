<template>
  <div>
    <Header />
    <FirstComponent />
    <LifeCycle />
    <Person />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import FirstComponent from "./components/FirstComponent.vue";
import LifeCycle from "./components/LifeCycle.vue";
import Person from './components/Person.vue';

export default {
  name: "App",
  components: {
    Header,
    FirstComponent,
    LifeCycle,
    Person,
  },
};
</script>

<style>
body {
  background-color: #333;
  color: #fff;
}

a {
  color: red;
}
</style>