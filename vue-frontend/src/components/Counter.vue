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
};
</script>

<style>
  button{
    color:white;
    border:none;
    background-color:#40b883;
    padding:10px;
    margin-left:10px;
    margin-right:10px;
    border-radius: 5px;
    transition: all 0.2s ease 0s;

  }
  button #decrement{
    background-color: red;
  }
  button:active{
    background-color:#273644;
  }

</style>

