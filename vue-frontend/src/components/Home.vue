<template>
  <div class="homecontainer">
    <!-- PART 1: Pass in a "complete" prop here -->
    <Instructions complete="done"/>
    <!-- PART 4: Modify the Show component to accept all of these props -->
    <Show
      v-for="show in shows"
      :key="show.id"
      :id="show.id"
      :name="show.name"
      :episodes_seen="show.episodes_seen"
    />
    <input v-model="message" placeholder="Name of show">
    <button type="button" v-on:click="addshow(message)">Submit</button>
  </div>
</template>

<script>
import Instructions from "./Instructions.vue";
import Show from "./Show.vue";

export default {
  components: {
    Instructions,
    Show
  },
  data() {
    return {
      shows: [
        { id: 1, name: "Game of Thrones", episodes_seen: 0 },
        { id: 2, name: "Naruto", episodes_seen: 220 },
        { id: 3, name: "Black Mirror", episodes_seen: 3 }
      ]
    };
  },
  methods : {
    addshow: function(message){
      this.shows.push({
        id: this.shows.length+1,
        name: message,
        episodes_seen: 0
      })
    }
  }
};
</script>

<style>
  .homecontainer{
    margin-bottom: 10vh;
  }
</style>


