<template lang="pug">
div(v-bind:key="task.id" v-for="task in tasks")
	h3 {{task.text}}
</template>
<script>
export default {
  name: 'Tasks',
  props: {
    tasks: Array,
  },
};
</script>
