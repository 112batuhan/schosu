<template>
  <div
    class="
      box-border
      h-5
      w-5
      p-4
      border-2 border-black
      rounded-lg
      flex-shrink-0
    "
    :class="colorString"
  ></div>
</template>


<script>
export default {
  name: "ScheduleBox",
  props: {
    colorString: String,
  },
};
</script>
