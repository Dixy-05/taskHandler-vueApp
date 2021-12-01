<template lang="pug">
div(v-bind:key="task.id" v-for="task in tasks")
	Task(@toggle-reminder="$emit('toggle-reminder',task.id)" v-on:delete-task="$emit('delete-task',task.id)" v-bind:task="task")
</template>
<script>
import Task from './Task.vue';
export default {
  name: 'Tasks',
  props: {
    tasks: Array,
  },
  components: { Task },
  //- this is to get rid of the warning in the console.It announces the events.(e.g. delete-task)
  emits: ['delete-task'],
};
</script>
