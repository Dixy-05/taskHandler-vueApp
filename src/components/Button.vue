<template lang="pug">

//- to add an event listener we can use v-on:click or @click
button.btn(v-bind:style="{ backgroundColor: color }" @click='onClick()') {{text}} 
</template>
<script>
import Tasks from './Tasks.vue';
export default {
  name: 'Button',
  //- in the props you can use either an array or an object
  props: {
    text: String,
    color: String,
  },
  methods: {
    onClick() {
      this.$emit('btn-click');
    },
  },
  components: {
    Tasks,
  },
};
</script>
<style>
.btn {
  color: white;
  margin-top: 1.5em;
  margin-bottom: 1.5em;
  border: none;
  border-radius: 10%;
  padding-right: 1em;
  padding-left: 1em;
  cursor: pointer;
}
</style>
