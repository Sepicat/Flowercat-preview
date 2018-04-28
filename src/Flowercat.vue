<template>
  <div id="app">
    <h1 v-html="msg"></h1>
    <input type="text" v-model="itemNew" v-on:keyup.enter="addNew" />

    <ul>
    </ul>
  </div>
</template>

<script>

import Storage from './localStorage'

export default {
  data () {
    return {
      msg: 'To-do list',      
      items: Storage.fetch(),
      
    }
  }
}
</script>
