<template>
  <div class="container">
    <Header title="Tasks"/>
    <AddTask />
    <Tasks @toggle-reminder="toggleReminder" @delete-task="deleteTask" :tasks="tasks"/>
  </div>
</template>

<script>
import Header from './components/Header'
import Tasks from './components/Tasks'
import AddTask from './components/AddTask'

export default {
  name: 'App',
  components: {
    Header,
    Tasks,
    AddTask
  },
  //methods
  methods: {
    //delete method
    deleteTask(id) {
      //pop up window to verify you want to delete
      if (confirm('Are you sure?')) {
        //return results of array if value does not == id
        this.tasks = this.tasks.filter((task) => task.id !== id)
      }
    },
    toggleReminder(id) {
      this.tasks = this.tasks.map((task) => task.id === id ? { ...task, reminder: !task.reminder } : task )
    }
  },
  //test data returning array 
  data() {
    return {
      tasks: []
    }
  },
  //populates tasks: []
  created() {
    //this can also contain json return via GET HTTP
    this.tasks = [
      {
      id: 1,
      text: 'Doctors Appointment',
      day: 'March 1st at 2:30pm',
      reminder: true,
      },
      {
        id: 2,
        text: 'Meeting at School',
        day: 'March 3rd at 1:30pm',
        reminder: true,
      },
      {
        id: 3,
        text: 'Shopping for Food',
        day: 'March 3rd at 11:30am',
        reminder: false,
      }
    ]
  }

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Poppins', sans-serif;
}

.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}

.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}

.btn:focus {
  outline: none;
}

.btn:active {
  transform: scale(0.98);
}

.btn-block {
  display: block;
  width: 100%;
}

</style>
