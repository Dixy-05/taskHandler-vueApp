<template lang="pug">
div(@dblclick="$emit('toggle-reminder',task.id)" v-bind:class="[task.reminder?'reminder':'','task']")
	h3.taskData {{task.text}}
		i.fas(@click="onDelete(task.id)") x
	p.taskData {{task.day}}
</template>
<script>
export default {
  name: 'Task',
  props: {
    task: Object,
  },
  methods: {
    onDelete(id) {
      this.$emit('delete-task', id);
    },
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
.reminder {
  border-left: 5px solid green;
}
.fas {
  color: red;
  font-size: 1.5em;
}
.fas:hover {
  color: rgb(243, 111, 23);
}
</style>
