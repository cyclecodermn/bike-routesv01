
// I added the tags below to import files.
<style src="./style.css"></style>
<template id='HelloWorld' src="./template.html"></template>

// More imports are in the main.js file
<script>
//import axios from "axios";
// import { get } from "http";
// import Axios from "https://unpkg.com/axios/dist/axios.min.js";
var url = "http://localhost:56150/GetByRowRange/5/10/";

export default {
  name: "HelloWorld",
  info: [],
  data: function() {
    return {
      results: []
    };
  },

  mounted() {
    axios.get(url).then(response => {
      this.results = response.data;
    });
  }
};

// function getData() {
//   window.setTimeout(function() {}, 3000);
//   let data = [];
//   // debugger;
//   return axios
//     .get(url)
//     .then(response => {
//       return response.data;
//     })
//     .catch(function() {});
// }
</script>