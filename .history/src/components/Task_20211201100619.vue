<template lang="pug">
div.task
	h3.taskData
		| {{task.text}}
		i(class="fas fa-times")

	p.taskData {{task.day}}
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
  margin-right: 2em;
}
.taskData {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.task.reminder {
  border-left: 5px solid green;
}
.fas {
  color: red;
}
</style>
