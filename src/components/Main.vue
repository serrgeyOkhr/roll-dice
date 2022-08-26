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
      <DiceComponent
        v-for="(dice, index) in data"
        :dice_value="index"
        :data="data"
        :key="index"
      />
    </div>
    <div class="actionPlate">
      <!-- selected dice + modifier + action button -->
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import DiceComponent from "./Dice.vue";

export default defineComponent({
  name: "MainComponent",
  components: {
    DiceComponent,
  },
  setup() {
    const data = ref({
      d20: 0,
      d12: 0,
      d10: 0,
      d8: 0,
      d6: 0,
      d4: 0,
      d2: 0,
      d100: 0,
    });
    return {
      data,
    };
  },
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.diceSelector {
  display: flex;
}
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
