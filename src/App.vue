<template>
  <div id="app">
   <hello-vue></hello-vue>
  </div>
</template>

<script>
import HelloWorldVue from "./components/HelloWorld.vue";

export default {
  components: {
    helloVue: HelloWorldVue
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
