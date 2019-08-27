
export default {
  name: "TableMethods",
  //info: [],
  data: 
  function() {
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