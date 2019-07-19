<template>

<div>
    <button @click="plus">+</button>
    <span>{{value}}</span>
    <button @click="minus">-</button>
</div>
</template>

<script>


export default {
  name: 'Counter',
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
    this.$emit("plus");
  },
  minus(){
    if(this.value>0){
      this.value--;
      this.$emit("minus");
    }
  }
  }

}
</script>