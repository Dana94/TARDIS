<template>
  <div id="app">
    <app-lamp></app-lamp>
    <app-roof></app-roof>
    <app-body></app-body>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Roof from './components/Roof.vue';
import Body from './components/Body.vue';
import Footer from './components/Footer.vue';
import Lamp from './components/Lamp.vue';

export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    appBody: Body,
    appFooter: Footer,
    appRoof: Roof,
    appLamp: Lamp
  }
}
</script>

<style lang="scss">
@import url('./assets/base.scss');
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

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
