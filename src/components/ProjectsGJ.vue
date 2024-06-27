<template>
  <div class="container p-0 md:p-10 md:p-2 md:px-20 m-auto">
    <h2 v-if="getCookie('lang') === 'eng'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Game Jam
      Projects</h2>
    <h2 v-if="getCookie('lang') === 'fr'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Projets de Game
      Jam</h2>
    <div class="flex flex-wrap justify-center">
      <Card
          :img1="AV1"
          link="https://gamevrest.odoo.com/"
          cardtitle="Premier Servi" year="2023" v-bind:tags="['Unity','Party Game', 'Steam']"
          desc="Premier Servi, use of AI generated assets, ongoing"
          descFR="Description de Premier servi en francais"
          longDesc="Long description for Premier servi"
          longDescFR="Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi"
      />
    </div>
  </div>
</template>


<script>
import AV1 from '@/assets/Projects/AV-1.jpg';

import Card from './Card.vue'
import {getCookie} from "@/cookie";

export default {
  name: 'ProjectsGJ',
  methods: {getCookie},
  components: {
    Card,
  },
  props: {
    msg: String
  },
  data() {
    return {
      AV1: Av1,
    }
  },
  mounted() {
    //this.PR = PR.toString();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
