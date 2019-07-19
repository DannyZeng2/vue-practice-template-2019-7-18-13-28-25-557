<template>
    <div>

        <div v-for="index of CounterNum" :key="index">
            <Counter></Counter>
        </div>
    </div>


</template>

<script>
import Counter from './Counter.vue';
export default {
  name: 'CounterGroup',
  props:['CounterNum'],
  components: {
    Counter
  },

  data(){
      return{
        value:0,
      }
  },

  methods:{
  
  }
}
</script>