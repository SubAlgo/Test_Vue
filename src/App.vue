<template>

<div>
  <input v-model="name">
  <p v-if="name && name !== 'korn'">Hi, {{ name }}</p>
  <p v-else-if="name === 'korn'">:D</p>
  <p v-else>No Data</p>
  <p v-for="x in list"> {{ x + ' ' +name }}</p>
  <button v-on:click="sayHello">Hello</button>
  <button @click="sayHello">@click</button>
</div>


</template>

<script>
export default {
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
