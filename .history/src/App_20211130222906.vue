<template>
  div.container
  <h1>Testing Vue.js</h1>
  <Header text="Testing Vue" color="green" />
  <Tasks v-bind:tasks="tasks" />
</template>

<script>
import Header from './components/Header.vue';
import Tasks from './components/Tasks.vue';
export default {
  name: 'App',
  components: { Header, Tasks },
  data() {
    return {
      tasks: [],
    };
  },
  //- created is life cycle similar to componentDidMount
  created() {
    this.tasks = [
      {
        id: 1,
        text: 'Doctors Appointment',
        day: 'March 1st at 2:30pm',
        reminder: true,
      },
      {
        id: 2,
        text: 'Meeting at school',
        day: 'March 3rd at 11:30am',
        reminder: true,
      },
      {
        id: 3,
        text: 'Food Shopping',
        day: 'March 3rd at 1:30pm',
        reminder: false,
      },
      {
        id: 4,
        text: 'Dentist Appointment',
        day: 'March 4th at 3:30pm',
        reminder: true,
      },
    ];
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
.btn {
  color: white;
}
</style>
