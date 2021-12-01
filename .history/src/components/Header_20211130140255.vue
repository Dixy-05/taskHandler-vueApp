<template lang="pug">
h1 {{title}}
.div
  p how are you?
  p I am good

	
</template>
<script>
export default {
  name: 'Header',
  props: ['title'],
};
</script>
<style scoped>
header {
  display: flex;
  justify-content: space-around;
}
</style>
