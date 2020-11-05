<template>
  <div class="hello">
    <h1>{{ msg }} (This Heading has been sent from other component as props) </h1>
     <div v-if="true">
        Usage of v-if directory.
    </div>
    <div v-show="true">
        Usage of v-show directory.
    </div>

    <span>Message: {{sampleMessage}}</span>

    <p> Displaying raw HTML : <i><b> {{ rawHtml }}</b></i></p>
    <p>Using v-html directive dispalying executable HTML: <span v-html="rawHtml"></span></p>

   <div v-bind:id="dynamicId()">Usage of v-bind </div>
  </div>
  
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data : () => { 
    return {
        sampleMessage: "This is the sameple message",
        rawHtml: "<h2 style='color:green'>RAW HTML</h2>",
        dynamicId: () => {
          return "bindId";
        }
    }
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.hello {
  text-align: center;
}
</style>
