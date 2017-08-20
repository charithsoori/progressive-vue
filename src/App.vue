<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <frameworkitem v-for="framework in frameworks" :data="framework" :key="framework"></frameworkitem>
  </div>
</template>

<script>
import frameworkitem from './components/framework.vue';

export default {
  name: 'app',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
      frameworks: ['Meteor', 'Angular 1', 'Angular 2', 'React'],
    }
  },
  components: {
    frameworkitem
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

h1,
h2 {
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
