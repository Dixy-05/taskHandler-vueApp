<template lang="pug">
div.header 
  h1 Testing Vue.js
  Button(text='Add Task' color='green')
</template>
<script>
import Button from './Button.vue';
export default {
  name: 'Header',
  //- in the props you can use either an array or an object
  props: {
    text: String,
    color: String,
  },
  components: { Button },
};
</script>
<style scoped>
.header {
  margin-top: 2em;
  display: flex;
  justify-content: space-around;
}
</style>
