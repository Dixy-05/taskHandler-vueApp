<template lang="pug">
h3 {{task.text}}
</template>
<script>
export default {
  name: 'Task',
  props: {
    task: Object,
  },
};
</script>
