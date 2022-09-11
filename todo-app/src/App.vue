
<template>
  <div class="container">
    <h3 class="text-center">Todo App</h3>
    <hr class="my-2"/>
    <label for="todo-text"></label>
    <input @keydown.enter="addNewTodo" type="text" placeholder="Type..." id="todo-text">
    <ul>
      <li v-for="item in todoList" :key="item.id" class="d-flex justify-content-between align-items-center"><span>{{ item.text }}</span><button @click="deleteItem(item)" class="sm red">X</button> </li>
    </ul>
    <small class="d-flex justify-content-end mt-2 green">There are {{todoList.length}} todo here.</small>
  </div>
</template>

<script>
export default{
  data(){
    return{
      todoList : [
        {id:1, text: "this is first todo"},
        {id:2, text: "this is second todo"},
        {id:3, text: "this is third todo"},
        {id:4, text: "this is fourth todo"},
        {id:5, text: "this is fifth todo"},
      ]
    }
  },
  methods : {
    deleteItem (todoItem){
      this.todoList = this.todoList.filter(t => t !== todoItem)
    },
    addNewTodo(e){
      this.todoList.push({
        id:new Date().getTime(),
        text: e.target.value
      });
      e.target.value = '';
    }
  }
}
</script>