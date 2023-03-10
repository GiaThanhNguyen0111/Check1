<template lang="">
    <div>
        <input type="text" v-model="newToDoItem"/>
        <button @click="addNewTodoItem()">Submit</button>
    </div>
</template>
<script>
export default {
    data() {
        return {
            newToDoItem: "",
        }
    },
    methods: {
        addNewTodoItem() {
            this.$store.dispatch('addNewToDo', this.newToDoItem);
            this.newToDoItem = "";
        },
    }
}
</script>
<style lang="">
    
</style>