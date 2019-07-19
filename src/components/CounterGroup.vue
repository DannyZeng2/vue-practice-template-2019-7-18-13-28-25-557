<template>
    <div>

        <div v-for="index of CounterNum" :key="index">
            <Counter @plus="plusCount" @minus="minusCount"></Counter>
        </div>
        <CounterSum :counterSum="sum"></CounterSum>
    </div>


</template>

<script>
import Counter from './Counter.vue';
import CounterSum from './CounterSum.vue';

export default {
  name: 'CounterGroup',
  props:['CounterNum'],
  components: {
    Counter,
    CounterSum
  },

  data(){
      return{
        sum:0,
      }
  },

  methods:{
    plusCount(){
      this.sum++;
    },

    minusCount(){
      this.sum--;
    }
  
  }
}
</script>