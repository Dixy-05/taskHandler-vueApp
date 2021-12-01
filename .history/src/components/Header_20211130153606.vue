<template lang="pug">
h1 {{title}}
.div
  p how are you?
  p I am good
  

	
</template>
<script>
export default {
  name: 'Header',
  //- in the props you can use either an array or an object
  props: {
    props: {
      text: String,
      color: String,
    },
  },
};
</script>
<style scoped>
header {
  display: flex;
  justify-content: space-around;
}
</style>
