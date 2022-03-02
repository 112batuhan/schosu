<template>
    <div class="flex flex-row flex-nowrap gap-0.5 sticky top-0">
      <div
        class="
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
          z-0
        "
      ></div>
      <div v-for="index in 15" :key="index">
        <div
          class="
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
            sticky left-0
            bg-white
          "
        >
          {{ index - 1 }}
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: "HourBar",
  props: {},
  components: {},
};
</script>
