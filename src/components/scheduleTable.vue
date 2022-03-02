<template>
  <div class="flex flex-col gap-0.5 flex-nowrap">
    <HourBar />
    <div class="container max-h-48 overflow-y-auto">
      <div
        v-for="index in 15"
        :key="index"
        class="flex gap-0.5"
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