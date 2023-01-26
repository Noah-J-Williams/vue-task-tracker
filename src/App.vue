<script>
  import Header from './components/Header.vue';
  import Button from './components/Button.vue';
  import Tasks from './components/Tasks.vue';

  export default{
    name: 'App',
    components: {
      Header,
      Tasks
    },
    data() {
      return {
        tasks: []
      }
    },
    created() {
      this.tasks = [
        {
          id: 1,
          text: "Doctors Appointment",
          day: "March 1st at 2:30pm",
          reminder: true,
        },
        {
          id: 2,
          text: "Meeting at School",
          day: "March 3rd at 1:30pm",
          reminder: true,
        },
        {
          id: 3,
          text: "Food Shopping",
          day: "March 3rd at 11:00am",
          reminder: false
        }
      ]
    }

  }
</script>

<template>
  <main class="container">
    <Header title="Task Tracker"/>
    <Tasks :tasks="tasks" />
  </main>
</template>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 75%;
  margin: 2.5rem auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 2.5rem;
  border-radius: 5px;
}

.btn {
  display: inline-block;
  background: black;
  color: white;
  border: none;
  padding: 1rem 1.75rem;
  margin: 1rem;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 1rem;
}
</style>
