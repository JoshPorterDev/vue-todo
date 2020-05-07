<template>
  <div id="app">
    <Navbar />
    <TaskList :tasks="listoftasks"/>
  </div>
</template>

<script>
import TaskList from './components/TaskList.vue'
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    TaskList
  },
  data()
  {
    return {
      listoftasks: [
        {id: 1, title: "learn HTML & CSS", completed: true},
        {id: 2, title: "learn Python", completed: false},
        {id: 3, title: "Make apps with django", completed: true}
      ]
    }
  }
}
</script>

<style>
* {
  padding: 0px;
  margin: 0px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
