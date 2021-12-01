<template lang="pug">
div(v-bind:key="task.id" v-for="task in tasks")
	h3 {{task.text}}
</template>
<script>
import Task from './Task.vue';
export default {
  name: 'Tasks',
  props: {
    tasks: Array,
  },
  components: { Task },
};
</script>
