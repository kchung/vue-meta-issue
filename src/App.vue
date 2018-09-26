<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',

	metaInfo() {
		return {
			title: this.title,
		};
	},

	data() {
		return {
			increment: 0,
			title: 'test',
		};
	},

	mounted() {
		setInterval(() => {
			// The title will *not* reactively update with 1.5.4
			this.title = `title-${this.increment++}`;
		}, 500);
	},

  components: {
    HelloWorld
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
