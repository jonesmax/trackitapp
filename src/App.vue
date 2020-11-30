<template>
  <div id="app">
        <status id="status"/>
        <tools id="tools"/>
        <items id="items"/>
  </div>
</template>

<script>
import status from './components/status.vue'
import tools from './components/tools.vue'
import items from './components/items.vue'

export default {
  name: 'App',
  components: {
    status,
    tools,
    items
  }
}
</script>

<style>
html,h1{
    margin: 0;
    padding: 0;
    border: none;
}
body { margin:0; } 
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
}
#status{
    background-color: rgb(123, 148, 155);
    width: 100%;
    
}
#tools{
    background-color: rgb(190, 190, 190);
}


</style>
