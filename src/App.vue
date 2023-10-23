<template>
  <MultiplicationTable />
</template>

<script>
import MultiplicationTable from './components/MultiplicationTable.vue'

export default {
  name: 'App',
  components: {
    MultiplicationTable
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
