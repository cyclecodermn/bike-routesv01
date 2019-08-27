
// I added the tags below to import files.
<style src="./style.css"></style>
<template id='ApiReader' src="./template.html"></template>

//The lines below didn't cause errs, but they also didn't to wwork.
// <script src="mockData.js" type="text/javascript"></script>
// <script src="searchTable.js" type="text/javascript"></script>

// More imports are in the main.js file
<script>
//import axios from "axios";
// import { get } from "http";
// import Axios from "https://unpkg.com/axios/dist/axios.min.js";
var url = "http://localhost:56150/GetByRowRange/5/10/";

export default {
  name: "ApiReader",
  //info: [],
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


//debugger
//results=getMockData();

function searchTable() {
  var input, filter, table, tr, td, i, txtValue;
  input = document.getElementById("myInput");
  filter = input.value.toUpperCase();
  table = document.getElementById("routesTable");
  tr = table.getElementsByTagName("tr");
  for (i = 0; i < tr.length; i++) {
    td = tr[i].getElementsByTagName("td")[1];
    if (td) {
      txtValue = td.textContent || td.innerText;
      if (txtValue.toUpperCase().indexOf(filter) > -1) {
        tr[i].style.display = "";
      } else {
        tr[i].style.display = "none";
      }
    }
  }
}

function getMockData() {
  return mockData;
}
</script>