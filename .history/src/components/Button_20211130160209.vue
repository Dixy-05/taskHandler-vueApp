<template lang="pug">
button.btn(v-bind:style="{ backgroundColor: color }") {{text}} 
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
