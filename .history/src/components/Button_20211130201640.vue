<template lang="pug">
//- to add an event listener we can use v-on:click or @click
button.btn(v-bind:style="{ backgroundColor: color }" @click='onClick()') {{text}} 
</template>
<script>
export default {
  name: 'Button',
  //- in the props you can use either an array or an object
  props: {
    text: String,
    color: String,
  },
  methods: {
    onClick() {
      console.log('something cool');
    },
  },
};
</script>
