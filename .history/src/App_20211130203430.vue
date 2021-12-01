<template>
  <h1>Testing Vue.js</h1>
  <Header text="Testing Vue" color="green" />
</template>

<script>
import Header from './components/Header.vue';
export default {
  name: 'App',
  components: { Header },
};
</script>

<style scope>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.btn {
  color: white;
}
</style>
