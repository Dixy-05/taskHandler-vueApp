<template lang="pug">
h1 {{title}}
button.btn {{text}}

</template>
<script>
export default {
  name: 'Header',
  //- in the props you can use either an array or an object
  props: {
    text: String,
    color: String,
  },
};
</script>
<style scoped>
header {
  display: flex;
  justify-content: space-around;
}
</style>
