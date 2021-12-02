<template lang="pug">
div.container
  Header(@toggle-addTask="toggleAddTask" text="Testing Vue" color="green" v-bind:show="showAddTask") 
  div(v-if="showAddTask")
    AddTask(@add-task="addTask") 
  Tasks(@toggle-reminder="toggleReminder"
    v-on:delete-task="deleteTask"
    v-bind:tasks="tasks")
    
 
</template>

<script>
import Header from './components/Header.vue';
import Tasks from './components/Tasks.vue';
import AddTask from './components/AddTask.vue';
export default {
  name: 'App',
  components: { Header, Tasks, AddTask },
  data() {
    return {
      tasks: [],
      showAddTask: false,
    };
  },
  methods: {
    async addTask(task) {
      const res = await fetch('api/tasks', {
        method: 'POST',
        headers: {
          'Content-type': 'application/json',
        },
        body: JSON.stringify(task),
      });
      const data = await res.json();
      this.tasks = [...this.tasks, data];
    },
    async deleteTask(id) {
      if (confirm('Are you sure?')) {
        const res = await fetch(`api/tasks/${id}`, {
          method: 'DELETE',
        });

        res.status === 200
          ? (this.tasks = this.tasks.filter((task) => task.id !== id))
          : alert('Error deleting task');
      }
    },
    toggleReminder(id) {
      this.tasks = this.tasks.map((task) =>
        task.id === id ? { ...task, reminder: !task.reminder } : task
      );
      // console.log(id);
    },
    toggleAddTask() {
      this.showAddTask = !this.showAddTask;
    },
    async fetchTasks() {
      // this is fetching from json-server (fake api) and
      // using vue.config.js we don't have to use 'http://localhost:5000' for fetch.
      const res = await fetch('api/tasks');
      const data = await res.json();
      return data;
    },
  },
  //- created is life cycle similar to componentDidMount
  async created() {
    this.tasks = await this.fetchTasks();
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  border: 2px black solid;
  padding-bottom: 2em;
}
</style>
