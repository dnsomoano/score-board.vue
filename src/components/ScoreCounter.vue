<template lang="html">
  <div>
    <section class="name-container">
      <h1>{{TeamNameDisplay}}</h1>
      <h1>{{TeamScore}}</h1>
      <input placeholder="update name" v-model="TeamName"></input>
      <button class="button-style" type="button" name="button" v-on:click="updateName">Update</button>
    </section>
      <section class="score-container">
      <button class="button-style" type="button" v-on:click="addOne">Add 1</button>
      <button class="button-style" type="button" v-on:click="subtractOne">Subtract 1</button>
    </section>
</div>
</template>

<script>
export default {
  data:function(){
    return {
      TeamName: "",
      TeamNameDisplay: "Team Name",
      TeamScore: 0
    }
  },
  methods:{
    updateName: function(){
      console.log(this);
      this.TeamNameDisplay = this.TeamName;
    },
    addOne: function(){
      this.TeamScore++;
    },
    subtractOne: function(){
      if (this.TeamScore > 0) {
        this.TeamScore--;
      }
    }
  }
}
</script>

<style lang="css">

.name-container {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
}

.score-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-start;
}

.button-style {
  border: 2px solid black;
  box-shadow: 0.5em 0.5em black;
  height: 3em;
  width: 9em;
}
</style>
