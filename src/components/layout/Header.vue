<template>
  <header class="header">
    <h1>TodoList</h1>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style>
  .header {
    background: linear-gradient(-45deg ,rgb(105, 187, 172),rgb(72, 72, 221),rgb(174, 37, 174)); 
    color: #fff;
    text-align: center;
    padding: 10px;
  }
  
  .header a {
    color: #fff;
    padding-right: 5px;
    text-decoration: none;
  }
</style>


