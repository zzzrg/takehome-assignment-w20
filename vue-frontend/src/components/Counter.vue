<template>

<div>
  <p>Number of episodes seen: {{count}}</p>
  <button v-on:click="count+=1">Increment</button>
  <button v-on:click="count-=1">Decrement</button>

</div>
</template>

<script>
export default {
  props:{
    count:Number
  },

  // data() {
  //   return {
  //     count: this.episodes,
  //   };
  // }
};
</script>

<style>
</style>

