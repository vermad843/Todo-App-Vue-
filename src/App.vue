<template>
  <div id="app" class = "container">
      <h1 class = "text-center">Todo App</h1>
      <form @submit.prevent = "addTodo()">
        <div class="form-group">
          <label for="newTodo">New Todo</label>
          <input
             v-model = "newTodo"
             type ="newTodo"
             class ="form-control"
             id ="newTodo"
             aria-describedby ="newTodoHelp"
             placeholder ="Enter Something"
             >
          <small
             id="newTodoHelp"
             class="form-text text-muted">
             Enter a newTodo
          </small>
        </div>
         <button
           type = "submit"
           class = "btn btn-primary"
           >
           Add Todo
        </button>
      </form>
      <ul class = "list-group mt-4">
         <li v-for = "todo in todos"
            class = "list-group-item"
           >
           {{todo}}
           <button
              type = "button"
              class = "btn btn-primary">
              done
            </button>
         </li>
      </ul>
  </div>
</template>
<script>
export default {
  name: 'app',
    data () {
      return {
         newTodo : '',
         todos : []
      }
    },
    methods : {
      addTodo() {
        this.todos.push(this.newTodo);
        this.newTodo = ''
      }
    }
  }
</script>

<style>

</style>
