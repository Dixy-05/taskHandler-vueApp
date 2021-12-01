<template lang="pug">

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
.btn {
  background-color: green;
  color: white;
}
</style>
