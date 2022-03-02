<template>
    <div class="flex flex-row gap-0.5">
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
