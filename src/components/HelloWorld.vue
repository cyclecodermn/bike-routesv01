
// I added the tags below to import files.
<style src="./style.css"></style>
<template id='HelloWorld' src="./template.html"></template>

// More imports are in the main.js file
<script>
import axios from "axios";
import { get } from "http";
// import Axios from "https://unpkg.com/axios/dist/axios.min.js";
var url = "http://localhost:56150/GetByRowRange/5/10/";
//var url = "https://min-api.cryptocompare.com/data/pricemulti?fsyms=BTC,ETH&tsyms=USD,EUR";

// export default {
//   name: "HelloWorld",
//   info: [],
//   data: function() {
//     return {
//       info: []
//     };
//   },
//   created: function() {
//     this.info = getData();
//   }
// };

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

// const vm = new Vue({
//   el: "#app",
//   data: {
//     results: []
//   },

//   mounted() {
//     axios.get(url).then(response => {
//       this.results = response.data;
//     });
//   }
// });

function getData() {
  window.setTimeout(function() {}, 3000);
  let data = [];
  debugger;
  return axios
    .get(url)
    .then(response => {
      return response.data;
    })
    .catch(function() {});
}

var mockData = [
  {
    RouteId: 10284626,
    RouteURL: "http://ridewithgps.com/routes/10284626",
    RouteName: "Tues Tuneup #5",
    RouteCity: "Minnetonka",
    RouteState: "MN",
    Distance: 37.5984268,
    ElevGain: 1280.21,
    LastModDate: "2019-06-16T00:00:00"
  },
  {
    RouteId: 15749508,
    RouteURL: "http://ridewithgps.com/routes/15749508",
    RouteName: "Mellow Mondays_NW_neighborhoods",
    RouteCity: "Roseville",
    RouteState: "MN",
    Distance: 29.2518559,
    ElevGain: 590.751343,
    LastModDate: "2019-04-11T00:00:00"
  },
  {
    RouteId: 18980794,
    RouteURL: "http://ridewithgps.com/routes/18980794",
    RouteName: "Orange Patch 35.0",
    RouteCity: "Mesa",
    RouteState: "AZ",
    Distance: 34.95878,
    ElevGain: 1005.02295,
    LastModDate: "2017-02-12T00:00:00"
  },
  {
    RouteId: 19280973,
    RouteURL: "http://ridewithgps.com/routes/19280973",
    RouteName: "Rio Verde - 50",
    RouteCity: "Fountain Hills",
    RouteState: "AZ",
    Distance: 50.02069,
    ElevGain: 2557.454,
    LastModDate: "2017-02-28T00:00:00"
  },
  {
    RouteId: 30365085,
    RouteURL: "http://ridewithgps.com/routes/30365085",
    RouteName: "Potawatomi Plus Little Sturgeon (copy)",
    RouteCity: "Sturgeon Bay",
    RouteState: "WI",
    Distance: 37.4983826,
    ElevGain: 1040.584,
    LastModDate: "2019-07-10T00:00:00"
  },
  {
    RouteId: 30365112,
    RouteURL: "http://ridewithgps.com/routes/30365112",
    RouteName: "2018 Door County Century Ride - 100 Mile (copy)",
    RouteCity: "Sturgeon Bay",
    RouteState: "WI",
    Distance: 99.99292,
    ElevGain: 2237.48364,
    LastModDate: "2019-07-05T00:00:00"
  }
];
</script>