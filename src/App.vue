<template>
  <div id="app">
    <h1>Testing <strong>Vue</strong> with <em>Jest</em></h1>
    <MessageList :messages="messages"/>
    <Form/>
  </div>
</template>

<script>
import MessageList from './components/MessageList'
import Form from './components/Form'

export default {
  name: 'app',
  data: () => ({ messages: [
    'Key Points of testing',
    'Tools & Configuration',
    'Testing Components',
    'Testing Utils Methods'
  ] }),
  components: {
    MessageList,
    Form
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px auto;
  overflow: hidden;
  width: 80%;
}
h1 {
    border: 5px solid #2c3e50;
    color: #34495f;
    padding: 20px;
}
h1 strong {
  color: #3ab981;
}

h1 em {
  color: #99424f;
}
</style>
