<template>
  <HelloWorld/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
html{
  height: 100%;
}
body{
 height: 100%;
}
#app{
  overflow: hidden;
}
</style>
