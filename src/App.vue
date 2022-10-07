<template>
  <dev class="title has-text-centered">
    Keng Todo
  </dev>
<br>
  <div class="field has-addons center">
  <div class="control">
    <input class="input" type="text" placeholder="Find a repository">
  </div>
  <div class="control">
    <a class="button is-info">
      Add
    </a>
  </div>
</div>


<div class="card center" v-for="todo in todos">
  <div class="card-content">
    <div class="content">
      {{todo.content}}
    </div>
  </div>
  <footer class="card-footer">
    <button href="#" class="card-footer-item button is-light">Save</button>
    <button href="#" class="card-footer-item button is-danger">Edit</button>
  </footer>
</div>

</template>
<script setup>
  import {ref} from 'vue'
  const todos = ref([
    {
      id:'id1',
      content: 'prepare dinner',
      done:false
    },
    {
      id:'id2',
      content: 'prepare interview',
      done:false
    },
    {
      id:'id3',
      content: 'test',
      done:false
    }
  ])
</script>

<style>
  @import 'bulma\css\bulma.min.css' ;
  .center {
    margin-left: auto;
    margin-right: auto;
    margin-top: 50px;
    width: 30em;
    overflow-wrap: break-word;
    overflow:hidden;
  }
</style>