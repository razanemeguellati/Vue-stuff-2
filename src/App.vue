<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <p> {{ title }} </p>
  <input type="text" ref="refname">
  <button @click="handleref"> show input</button>
</template>

<script>
// the styles are global
// exporting object : a root component
export default {
  name: 'App',
  components: {
    // any extra components we used    
  }, 

  data(){
    return {
      title: 'My first vue app '
    }
  },

  methods: {
    handleref(){
      // we can use this to change dom elements display (focus is pretty self-explanatory)
      // and we'll also use them for composition api 
      this.$refs.refname.focus()
    }
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
  margin-top: 60px;
}
</style>
