<template>

<div>
  <input v-model="name">
  <Hello v-bind:name="name"></Hello>
  <Hello :name="name"></Hello>
</div>


</template>

<script>
import Hello from './Hello'
export default {
  components: {
    Hello
  },
  data () {
    return {
      name: '',
      list: [
        1, 2, 3, 4, 5
      ]
    }
  },
  methods: {
    sayHello () {
      window.alert('Im,' + this.name)
    }
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
  margin-top: 60px;
}
</style>
