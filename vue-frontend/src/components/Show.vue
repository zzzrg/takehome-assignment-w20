<template>
  <!-- PART 4: Add your code here -->
  <div class="shows">
    <p id="title">{{name}}</p>
    <Counter v-bind:count="episodes_seen"/>
    <br />
  </div>
</template>

<script>
// PART 4: Add your code here
import Counter from "./Counter"

export default {
  components:{
    Counter
  },

  props: {
    id: Number,
    name: String,
    episodes_seen: Number
  },
};
</script>

<style scoped>
  #title{
    font-weight:bold;
  }
  .shows{
    background-color:#35495d;
    color:white;
    padding-top:2em;
    margin:2em auto;
    width:25em;
    border-radius:10px;
    left:50%
  }
</style>
