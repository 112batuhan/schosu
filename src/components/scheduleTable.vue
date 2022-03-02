<template>
  <div class="flex flex-col gap-0.5 flex-nowrap">
     <div
        class="
          fixed top-0 left-0
          h-5
          w-5
          p-4
          flex
          justify-center
          items-center
          flex-shrink-0
          text-xl
          font-bold
          border-2 border-transparent
          bg-white
          z-10
        "
      ></div>
    <HourBar />
    <div class="container">
      <div
        v-for="index in 15"
        :key="index"
        class="flex flex-row gap-0.5"
      >
        <div
          class="
            h-5
            w-5
            p-4
            flex flex-col
            justify-center
            items-center
            flex-shrink-0
            text-xl
            font-bold
            border-2 border-transparent
            sticky 
            left-0
            bg-white
            z-0
          "
        >
          {{ index }}
        </div>
        <DayRow />
      </div>
    </div>
  </div>
</template>


<script>
import DayRow from "./dayRow.vue";
import HourBar from "./hourBar.vue";

export default {
  name: "ScheduleTable",
  props: {},
  components: {
    DayRow,
    HourBar,
  },
};
</script>