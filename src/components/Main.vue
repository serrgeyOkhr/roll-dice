<template>
  <div class="container">
    <h1>Roll Dice</h1>
    <q-separator />
    <div class="diceTray">
      <!-- Here will be a dice results -->
    </div>
    <div class="savedRolls">
      <!-- Saved rolls -->
      <div class="savedRoll">
        <!-- v-for='(roll, index)' in rolls :key=index -->
      </div>
    </div>
    <div class="diceSelector">
      <!-- active selector component -->
    </div>
    <div class="actionPlate">
      <!-- selected dice + modifier + action button -->
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "MainComponent",
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
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
