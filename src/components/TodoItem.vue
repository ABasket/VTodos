<template>
    <div class="todo-item" :class="{'is-complete':todo.completed}">
        <p>
            <input type="checkbox" @change="markComplete" />
              {{todo.title}}
              <button class="del" @click="$emit('deleteItem',todo.id)">删除</button>
        </p>
      
    </div>
</template>
<script>
export default {
    name: "todoitem",
    data() {
        return {

        }
    },
    props:["todo"],
    methods:{
        markComplete() {
            this.todo.completed = !this.todo.completed
        }
    }
}
</script>
<style scoped>
 .todo-item {
     background-color: #f4f4f4;
     padding: 10px;
     border-bottom: 1px dotted #ccc;
 }
 .is-complete{
     text-decoration: line-through;
 }
</style>


