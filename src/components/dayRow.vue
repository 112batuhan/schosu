<template>
  <div class="flex flex-row gap-0.5">
    <schedule-box
      v-for="state in states"
      v-bind:key="state.id"
      @click="changeState(state.id)"
      :colorString="colors[state.value]"
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

      states: [
        { id: 0, value: 0 },
        { id: 1, value: 1 },
        { id: 2, value: 2 },
        { id: 3, value: 3 },
        { id: 4, value: 0 },
        { id: 5, value: 1 },
        { id: 6, value: 2 },
        { id: 7, value: 2 },
        { id: 8, value: 2 },
        { id: 9, value: 2 },
        { id: 10, value: 2 },
        { id: 11, value: 2 },
        { id: 12, value: 2 },
        { id: 13, value: 2 },
        { id: 14, value: 2 },
      ],
    };
  },

  props: {},

  methods: {
    changeState: function (id) {
      if (this.states[id].value++ > 3) {
        this.states[id].value = 0;
      }
      console.log("colorchange wohoo " + this.states[id].value); // returns 'foo'
    },
  },

  components: {
    ScheduleBox,
  },
};
</script>
