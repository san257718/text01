<template>
  <div class="border flex flex-col w-full lg:flex-row lg:max-w-[1248px] lg:h-[270px] min-h-[546px] lg:min-h-0">
    <div class="flex-none lg:h-full aspect-video">
      <img :src="`../image/${img}`" alt="" class="h-full w-full object-cover" />
    </div>
    <div class="flex-1 px-6 flex flex-col justify-center gap-6">
      <div class="flex">
        <span class="border bg-gray-200 text-sm p-0.5 block">{{ type }}</span>
      </div>
      <div class="flex flex-col gap-2">
        <p class="font-bold text-lg">{{ name }}</p>
        <p class="text-sm">{{ time }}</p>
        <p class>{{ content }}</p>
      </div>
      <div class="flex flex-row justify-center gap-4">
        <button class=" border text-lg flex justify-center items-center p-2 mx-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
            
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M10 19l-7-7m0 0l7-7m-7 7h18"
            />
          </svg>
        </button>
        <button class="border text-lg flex justify-center items-center p-2 mx-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
            
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M14 5l7 7m0 0l-7 7m7-7H3"
            />
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  props: ["id", "name", "img", "content", "type", "time"],
  data() {
    return {
      slides: true
    };
  },
}
</script>

<style>

</style>