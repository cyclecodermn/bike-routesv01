
// I added the tags below to import files.
<style src="./style.css"></style>
<template src="./template.html"></template>

// More imports are in the main.js file

<script>

function returnSomething() {

return `This is something.`

}

var mockData= [
    {
        "RouteId": 10284626,
        "RouteURL": "http://ridewithgps.com/routes/10284626",
        "RouteName": "Tues Tuneup #5",
        "RouteCity": "Minnetonka",
        "RouteState": "MN",
        "Distance": 37.5984268,
        "ElevGain": 1280.21,
        "LastModDate": "2019-06-16T00:00:00"
    },
    {
        "RouteId": 15749508,
        "RouteURL": "http://ridewithgps.com/routes/15749508",
        "RouteName": "Mellow Mondays_NW_neighborhoods",
        "RouteCity": "Roseville",
        "RouteState": "MN",
        "Distance": 29.2518559,
        "ElevGain": 590.751343,
        "LastModDate": "2019-04-11T00:00:00"
    },
];

export default {
  name: 'HelloWorld',
  data() {
    return {
    otherMsg: 'This is another message.',
    apiData1: returnSomething(),
    apiData2: mockData,
    };
  },
props: {
    msg: String
  }
}



</script>