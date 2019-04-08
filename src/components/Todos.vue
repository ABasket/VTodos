<template>
    <div>
        <div v-for="(todo,index) in todos" :key="index">
            <!-- <TodosItem :todo="todo" @deleteItem="deleteItem" /> -->
            <TodosItem :todo="todo" @deleteItem="$emit('handleDelete',todo.id)" />
        </div>
    </div>
</template>
<script>
import TodosItem from './TodoItem'
export default {
    name: "todos",
    data() {
        return {

        }
    },
    props:{
        todos:{
            type: Array
        }
    },
    components:{
        TodosItem
    }
}
</script>
<style scoped>

</style>


