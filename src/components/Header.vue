<template lang="pug">
div.header 
  h1 Testing Vue.js
  Button(@btn-click="$emit('toggle-addTask')" v-bind:text="show?'Close':'Add Task'" v-bind:color="show?'red':'green'")
</template>
<script>
import Button from './Button.vue';
export default {
  name: 'Header',
  //- in the props you can use either an array or an object
  props: {
    // text: String,
    // color: String,
    show: Boolean,
  },
  components: { Button },
  emits: ['toggle-addTask'],
};
</script>
<style scoped>
.header {
  margin-top: 2em;
  display: flex;
  justify-content: space-around;
}
</style>
