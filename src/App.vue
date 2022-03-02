<template>
  <div class="container max-w-40 max-h-40">
    <ScheduleTable />
  </div>
</template>


<script>
import ScheduleTable from "./components/scheduleTable.vue";

export default {
  name: "App",
  components: {
    ScheduleTable,
  },
};
</script>

