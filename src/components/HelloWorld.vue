<template>
  <div class="hello">
    <textarea
      v-model="textVal"
       cols="70" rows="40"
      class="textMsg"
    ></textarea>
    <br>
    <button @click="convert()">covert</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      textVal: ""
    };
  },
  methods: {
    convert(){
      this.textVal = this.textVal.replaceAll("<br>", " ").replaceAll("&nbsp;", " ").replaceAll("&lt;", "<").replaceAll("&gt;", ">").replaceAll("&le;", "≤ ").replaceAll("&ge;", "≥").replaceAll("&amp;", "&");
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
.textMsg {
  resize: both;
  overflow: auto;
}
</style>
