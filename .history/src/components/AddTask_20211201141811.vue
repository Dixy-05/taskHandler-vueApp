<template lang="pug">
div.container
	form.add-form
		
		div.form-control
			label Task
			input(type='text' name='text' placeholder='Task')
		div.form-control
			label Day & Time
			input(type="text" name="date" placeholder="Add Day & Time")
		div.form-control(class='form-control-check')
			label Set Reminder
			input(type='checkbox' name='reminder')
	input(class='btn-block' type='submit' value='Save Task')
</template>
<script>
export default {
  name: 'AddTask',
};
</script>
<style>
.container {
  margin-left: 2em;
  margin-right: 2em;
  border: none;
}
.form-control {
  text-align: start;
}
.btn-block {
  color: white;
  background: black;
  border: none;
  /* padding: 1em 25em 1em 25em; */
  border-radius: 5px;
}
</style>
