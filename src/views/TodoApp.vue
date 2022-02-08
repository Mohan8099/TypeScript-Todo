<template>
  <div class="container">
    <h1 class="text-center mt-5">To-do App</h1>

    <div class="d-flex">
      <input v-model="todo" type="search" placeholder="What's the task for now ...." class="form-control m-3">
      <button @click="addTodo" class="btn btn-primary rounded-1 m-3">ADD</button>
    </div>

    <table class="table table-bordered m-3">
      <thead>
        <tr>
          <th scope="col" class="w-50 text-center">Todo</th>
          <th scope="col" class="w-25 text-center">Staus</th>
          <th scope="col" class="w-25 text-center">Edit Task</th>
          <th scope="col" class="w-25 text-center">Remove</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(todo, index) in todos" :key='index' :class="{ 'todo-done': todo.status === 'Done' }">
          <th class="w-50 text-center" :class="{ 'text-success text-white': todo.status === 'Done' }">
        {{todo.todotask}}
        </th>
      <td class="w-25 text-center">
        <span @click="updateStatus(index)" class="pointer">{{todo.status}}</span>
        </td>
      <td class="w-25 text-center">
        <div>
          <button class="btn" @click="editTodo(index)">
            <span class="fa fa-pen"></span>
          </button>
        </div>
      </td>
      <td class="w-25 text-center">
        <div>
          <button class="btn" @click="removeTodo(index)">
            <span class="fa fa-trash" ></span>
          </button>
        </div>
      </td>
        </tr>
      </tbody>
    </table>

  </div>
</template>

<script lang="ts">
export default {
  name: 'To do App',
  props: {
    msg: String
  },
  data() {
    return {
      todo: '',
      statusList: ['To-do', 'In-Progress', 'Done'],
      editedTodo: '',
      todos: []
    }
  },
  methods: {
    addTodo() {
      if (this.todo.length === 0) {
        alert('Enter a task to add')
      } 
      else if (this.editedTodo === ''){
        this.todos.push({
          todotask: this.todo,
          status: 'To-do'
        })
        this.todo = ''
      } else {
        this.todos[parseInt(this.editedTodo)].todotask = this.todo
        this.editedTodo = ''
        this.todo = ''
      }
      
    },

    removeTodo(index: number) {
      alert('Are you sure you want to remove this from your To-di list ?')
      this.todos.splice(index, 1)  
    }, 

    updateStatus(index: string|number) {
      let newIndex = this.statusList.indexOf(this.todos[index].status)
      if (++newIndex > 2) newIndex = 0
      this.todos[index].status = this.statusList[newIndex]
    },

    editTodo(index: string | number) {
      this.todo = this.todos[index].todotask
      this.editedTodo = index.toString()
    }
  }
}
</script>

<style scoped>

.pointer {
  cursor: pointer;
}

.todo-done {
  background-color: #42b983;
}

</style>

