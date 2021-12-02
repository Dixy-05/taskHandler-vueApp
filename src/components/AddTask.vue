<template lang="pug">
div.container
	form.add-form(@submit="onSubmit")
		div.form-control
			label Task
			input.input(type='text' v-model="text" name='text' placeholder='Task')
		div.form-control
			label Day & Time
			input.input(type="text" v-model="day" name="date" placeholder="Add Day & Time")
		div.form-control(class='form-control-checkbox')
			label 
				b Set Reminder
			input.checkbox(type='checkbox' v-model="reminder" name='reminder')
		input(class='btn-block' type='submit' value='Save Task')
</template>
<script>
export default {
  name: 'AddTask',

  data() {
    return {
      text: '',
      day: '',
      reminder: false,
    };
  },
  methods: {
    onSubmit(e) {
      e.preventDefault();
      if (!this.text) {
        alert('Please add a task');
        return;
      }
      const newTask = {
        // this type of id is only for the example, should not be used in real app
        // id: Math.floor(Math.random() * 100000),
        //id will be added by json-server(fake api)
        text: this.text,
        day: this.day,
        reminder: this.reminder,
      };

      this.$emit('add-task', newTask);

      // To clear the form
      this.text = '';
      this.day = '';
      this.reminder = false;
    },
  },
};
</script>
<style scoped>
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
  padding: 0.7em 0.7em;
  border-radius: 5px;
  width: 100%;
  cursor: pointer;
}
.add-form {
  margin-bottom: 1em;
}
</style>
