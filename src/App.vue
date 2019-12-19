<template>
  <div id="app" class = "container">
      <h1 class = "text-center">Todo App</h1>
      <form @submit.prevent = "addTodo()">
        <div class="form-group">
          <label for="newTodo">New Todo</label>
          <input
             type="newTodo"
             class="form-control"
             id="newTodo"
             aria-describedby="newTodoHelp"
             placeholder="Enter Something"
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
  </div>
</template>
<script>
export default {
  name: 'app',
    data () {
      return {

      }
    },
    methods : {
      addTodo() {
        console.log('form submitted')
      }
    }
  }
</script>

<style>

</style>
