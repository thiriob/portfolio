<template>
  <swiper :navigation="true" :modules="modules" class="bg-gray-200 rounded">
    <swiper-slide v-if="video" >
      <div class="flex justify-center my-4 h-full w-full rounded">
        <iframe :src="video" height="360" width="80%"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin" allowfullscreen class="rounded-lg"
        ></iframe>
      </div>
    </swiper-slide>

    <swiper-slide>
      <div class="flex justify-center my-4">
        <img
            v-bind:src="img1"
            v-bind:alt="img1"
            class="object-cover max-h-80 rounded select-none"
        />
      </div>
    </swiper-slide>
    <swiper-slide v-if="img2">
      <div class="flex justify-center my-4"><img
          v-bind:src="img2"
          v-bind:alt="img2"
          class="object-cover max-h-80 rounded select-none"
      />
      </div>
    </swiper-slide>
    <swiper-slide v-if="img3">
      <div class="flex justify-center my-4"><img
          v-bind:src="img3"
          v-bind:alt="img3"
          class="object-cover max-h-80 rounded select-none"
      />
      </div>
    </swiper-slide>
  </swiper>
</template>
<script>
// Import Swiper Vue.js components
import {Swiper, SwiperSlide} from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
import 'swiper/css/navigation';
import {Navigation} from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  props: {
    img1: String,
    img2: String,
    img3: String,
    video: String,
  },
  setup() {
    const onSwiper = (swiper) => {
      console.log(swiper);
    };
    const onSlideChange = () => {
      console.log('slide change');
    };
    return {
      modules: [Navigation],
      onSwiper,
      onSlideChange,
    };
  },
};
</script>