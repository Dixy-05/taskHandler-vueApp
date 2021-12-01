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
<style>
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
  margin-left: 2em;
}
</style>
