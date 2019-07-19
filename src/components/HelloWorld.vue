<template>

  <div class="hello">
    <div>
      <input id="count" v-model.number="num">
      <CounterGroup :CounterNum ="num"></CounterGroup>
    </div>
  </div>

</template>

<script>
import CounterGroup from './CounterGroup.vue';
export default {
  name: 'HelloWorld',
  props: {

  },

  components: {
    CounterGroup,
  },

  data(){
    return {
      num:0
    }
  },

  methods:{
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
