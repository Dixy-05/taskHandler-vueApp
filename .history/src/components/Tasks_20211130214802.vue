<template lang="pug">
div(v-for="task in tasks")
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
