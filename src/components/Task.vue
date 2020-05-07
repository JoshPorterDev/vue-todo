<template>
    <div class="todo-item" :class="{'is-complete':aTask.completed}">
        <input type="checkbox" v-on:click="complete">
        <p>{{ aTask.title }}</p>
    </div>
</template>

<script>
export default {
    name: "Task",
    props: ['aTask'],
    methods: 
    {
        complete: function()
        {
            this.aTask.completed = !this.aTask.completed;
        }
    }
}
</script>

<style scoped>
.todo-item {
    background: #f4f4f4;
    padding: 10px;
    border-bottom: 1px #ccc dotted;
}

.is-complete {
    text-decoration: line-through;
}
</style>