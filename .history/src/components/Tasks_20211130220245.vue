<template lang="pug">
div(v-bind:key="task.id" v-for="task in tasks")
	Task(v-bind:task="task")
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
