<template lang="pug">
div.task
	h3 {{task.text}}
	p {{task.day}}
</template>
<script>
export default {
  name: 'Task',
  props: {
    task: Object,
  },
};
</script>
