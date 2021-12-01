<template lang="pug">
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
header {
  display: flex;
  justify-content: space-around;
}
</style>
