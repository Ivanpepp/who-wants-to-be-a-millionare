<template>
  <div class="hello">
    <div>
      <h1>{{Asks[indexCounter].request}}</h1>
      <ul>
        <li @click="isCurrect(Asks[indexCounter].answer1)"   class="btn btn-secondary">{{Asks[indexCounter].answer1}}</li>
        <li @click="isCurrect(Asks[indexCounter].answer2)"    class="btn btn-secondary">{{Asks[indexCounter].answer2}}</li>
        <li @click="isCurrect(Asks[indexCounter].answer3)"    class="btn btn-secondary">{{Asks[indexCounter].answer3}}</li>
        <li @click="isCurrect(Asks[indexCounter].answer4)"    class="btn btn-secondary">{{Asks[indexCounter].answer4}}</li>
      </ul>
    </div>
  </div>
</template>

<script>

import Asks from '../data/ask.js'
export default {
  name: "HelloWorld",
  data: function(){
    return{
      Asks,
      indexCounter: 0,
    }
  },
  methods:{
    isCurrect: function(answer){
      if(answer == this.Asks[this.indexCounter].exact){
        alert('risposta esatta');
      }else{
        alert('risposta sbagliata');
      }
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
</style>
