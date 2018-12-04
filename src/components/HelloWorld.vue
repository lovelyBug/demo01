<template>
  <div class="hello">
    <ul>
      <li v-bind:key="todo.text" v-for="todo in todos">
        {{ todo.text }}
      </li>
    </ul>
    <p>{{ message }}</p>
    <p>{{ reverseMessage }}</p>
    <input v-model="message">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      todos: [
        {text: 'JS'},
        {text: 'CSS'},
        {text: 'HTML'}
      ],
      message: 'Hello vue!'
    }
  },
  computed: {
    reverseMessage () {
      return this.message.split('').reverse().join('')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
