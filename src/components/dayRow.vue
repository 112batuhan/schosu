<template>
  <div class="flex flex-row gap-0.5">
    <schedule-box
      v-for="(state, index) in states"
      v-bind:key="state"
      @click="changeState(index)"
      :colorString="colors[state]"
    />
  </div>
</template>
<script>
import ScheduleBox from "./scheduleBox.vue";

export default {
  name: "DayRow",
  data: function () {
    return {
      colors: ["bg-red-600", "bg-green-600", "bg-yellow-500", "bg-gray-500"],
      states: [1, 2, 3, 1, 2, 3, 0, 1, 2, 3, 0, 0, 0, 0, 0],
    };
  },

  props: {},

  methods: {
    changeState: function (index) {
      if (this.states[index]++ > 3) {
        this.states[index] = 0;
      }
      console.log("colorchange wohoo " + this.states[index]); // returns 'foo'
    },
  },

  components: {
    ScheduleBox,
  },
};
</script>
