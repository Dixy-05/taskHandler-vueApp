<template lang="pug">
div.container
	form.add-form
		
		div.form-control
			label Task
			input.input(type='text' name='text' placeholder='Task')
		div.form-control
			label Day & Time
			input.input(type="text" name="date" placeholder="Add Day & Time")
		div.form-control(class='form-control-checkbox')
			label 
				b Set Reminder
			input.checkbox(type='checkbox' name='reminder')
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
  display: flex;
  flex-direction: column;
  text-align: start;
  margin-bottom: 0.5em;
}
.form-control-checkbox {
  display: flex;
  flex-direction: row;
}
.checkbox {
  margin-left: 20em;
  height: 15px;
  width: 15px;
}
.input {
  margin-top: 5px;
  border: 1px black solid;
  border-radius: 5px;
  padding: 0.5em 0.5em;
}
.btn-block {
  color: white;
  font-size: 1em;
  background: black;
  border: none;
  padding: 1em 45% 1em 45%;
  border-radius: 5px;
}
.add-form {
  margin-bottom: 1em;
}
</style>
