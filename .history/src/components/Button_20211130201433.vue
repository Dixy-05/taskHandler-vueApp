<template lang="pug">
button.btn(v-bind:style="{ backgroundColor: color }" v-on:click='onClick()') {{text}} 
</template>
<script>
export default {
  name: 'Button',
  //- in the props you can use either an array or an object
  props: {
    text: String,
    color: String,
  },
};
</script>
