<template>
  <div class="TaskList">
    <ul>
      <li v-for="task in tasks" v-bind:key="task.id">
        <Task :aTask="task"/>
      </li>
    </ul>

  </div>
</template>

<script>
import Task from './Task.vue'
export default {
  name: 'TaskList',
  props: ['tasks'],
  components: {
    Task
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: block;
  margin: 0 10px;
  margin-top: 10px;
}
a {
  color: #42b983;
}
</style>
