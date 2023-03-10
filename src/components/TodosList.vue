<template>
    <div>
        <TodoItem v-for="(todo, key) in todos" :key="key" :todo="todo"/>
    </div>
</template>

<script>
import TodoItem from "./Todo.vue";
export default {
    components: {
        TodoItem
    },
    computed: {
        todos: function(){
            return this.$store.state.todos;
        }
    }

 
}
</script>

<style>
</style>