<template>
    HALAMAN INDEX 3
    <div id="app">
    <split-carousel>
      <split-carousel-item v-for="item in 8" :key="item">
        {{ item }}
      </split-carousel-item>
    </split-carousel>
  </div>
</template>


<script >
import { SplitCarousel, SplitCarouselItem } from "vue-split-carousel";
  export default {
    components: {
      SplitCarousel,
      SplitCarouselItem
    }
  };

  // const app = Vue.createApp({
  //   template:`
  //     <split-carousel>
  //       <split-carousel-item v-for="i in 8">{{i}}</split-carousel-item>
  //     </split-carousel>
  //   `
  // })
  // app.use(window['vue-split-carousel'])
  // app.mount('#app')

  </script>

