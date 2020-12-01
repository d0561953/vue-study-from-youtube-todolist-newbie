<template>
  <div>
    <form @submit.prevent="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add Todo...">
      <input type="submit" value="Submit" class="btn">
    </form>
  </div>
</template>

<script>
// import uuid from 'uuid';
export default {
  name: "AddTodo",
  data() {
    return {
      title: ''
    }
  },
  methods: {
    addTodo() {
      const newTodo = {
        title: this.title,
        completed: false
      }
      // Send up to parent
      this.$emit('add-todo', newTodo);

      this.title = '';
    }
  }
}
</script>

<style scoped>
  form {
    display: flex;
    padding: 5px;
    margin: 10px 0px;
  }

  input[type="text"] {
    flex: 10;
    padding: 12px 20px;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1rem;
  }

  input[type="submit"] {
    flex: 2;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1rem;
  }
</style>


