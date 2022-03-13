<template>
  <header_1 />


  <div class="h-full flex justify-center">
    <div class="py-5 px-5 border">
      <button @click="type = ''">全部</button>
    </div>
    <div class="py-5 px-5 border">
      <button @click="type = '甜點'">甜點</button>
    </div>
    <div class="py-5 px-5 border">
      <button @click="type = '主食'">主食</button>
    </div>
  </div>


  <div
    class="w-full h-full grid grid-cols-1 md:grid-cols-2 gap-10 lg:grid-cols-1 justify-items-center py-20 px-10 mx:top-10 mx:relative"
    >
      <card v-for="item in getDatas" :key="item.id" v-bind="item" class="slides mx:absolute mx:overflow-hidden bg-slate-100"/>
  </div>

  
</template>

<script>
import header_1 from "../components/header_1.vue";
import card from "../components/card.vue";
import food from "../assets/food.json";
export default {
  data() {
    return {
      items: food,
      type: "",
    };
  },

  components: {
    card,
    header_1,
    food,
  },
  computed: {
    getDatas() {
      if (this.type) {
        return this.items.filter((e) => {
          return e.type === this.type;
        });
      } else {
        return this.items;
      }
    },
  },
};
</script>

<style>


.slides{
  animation: tada 1s;
}

.slides:active{
  animation: none;
}



@keyframes tada {
  0% {
    from: translateX(0%);
  }
  100%{
    to: translateX(-100%);
  }
}

@keyframes tada {
  0% {
    opacity: 1
  }
  100%{
    opacity: 0
  }
}






</style>