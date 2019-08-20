// I added the tags below to import files.
<style src="./style.css"></style>
<template src="./template.html"></template>

// More imports are in the main.js file

<script>

  function returnSomething2() {

  return `This is something.`

  }

  export default {
    name: 'ApiData',
    data() {
      return {
      otherMsg2: 'This is another message.',
      apiData12: returnSomething2(),
      };
    },
  props: {
      msg: String
    }
  }

</script>