<template>
  <div class="hello">
    <button @click="plus">+</button>
    <input v-model="value"/>
    <button @click="minus">-</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String

  },

  data(){
      return{
        value:0,
      }
  },

  methods:{
  plus(){
    this.value++;
  },
  
  minus(){
    if(this.value>0){
      this.value--;
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
</style>
