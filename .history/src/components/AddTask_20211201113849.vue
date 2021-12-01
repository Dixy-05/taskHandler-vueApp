<template lang="pug">
form.add-form
	div.form-control
		label Task
		input(type='text' name='text' placeholder='Add Day & Time')
	div.form-control(class='form-control-check')
		label Set Reminder
		input(type='checkbox' name='reminder')
	input(class='btn btn-block' type='submit' value='Save Task')
</template>
