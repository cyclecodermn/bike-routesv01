
// I added the tags below to import files.
<style src="./style.css"></style>
<template src="./template.html"></template>
<script src="./api-data.js"></script>

// More imports are in the main.js file

<script>

function returnSomething() {

return `This is something.`

}



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