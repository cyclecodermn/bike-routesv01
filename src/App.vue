<template>
  <div id="app">
    <ApiReader msg="Welcome to TCBC Bike Routes" />
  </div>
</template>

<script>
import ApiReader from "./components/ApiReader.vue";
import TableMethods from "./components/TableMethods.vue";

export default {
  name: "app",
  components: {
    ApiReader,
    TableMethods
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
