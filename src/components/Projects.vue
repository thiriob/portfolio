<template>
  <div class="container p-0 md:p-10 md:p-2 md:px-20 m-auto">
    <h2 v-if="getCookie('lang') === 'eng'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Featured
      Projects</h2>
    <h2 v-if="getCookie('lang') === 'fr'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Projets en
      vedette</h2>
    <div class="flex flex-wrap justify-center">
      <Card
          :img1="PS1"
          :img2="PS2"
          :img3="PS3"
          link="https://gamevrest.odoo.com/"
          cardtitle="Premier Servi" year="2023" v-bind:tags="['Unity','Party Game', 'Steam']"
          desc="Colorful party game taking inspiration from French culture."
          descFR="Party Game coloré tirant inspiration de la culture française."
          longDesc=""
          longDescFR="dfslgjihjfsoghsfljgolsfjikgs adjbfsd sd  sfdg sfdgds f gdf g dfgf fd"
      />
      <Card
          :img1="AV1"
          cardtitle="Aviator" year="2023" v-bind:tags="['Unity', 'Android', 'Firebase', 'Narrative']"
          desc="Mobile Game, tower defense like, usage of AI generated images"
          descFR="Description de Aviator en francais"
          longDesc="Premier Servi, use of AI generated assets, ongoing"
          longDescFR="Premier Servi, use of AI generated assets, on`going"
      />
      <Card
          video="https://www.youtube.com/embed/HJnT_nsFjWY"
          :img1="PC1"
          :img2="PC2"
          :img3="PC3"
          cardtitle="Proxima Cities" year="2020" v-bind:tags="['Unity', 'AR', 'City Builder']"
          desc="Augmented reality city, on mobile application"
          descFR="Description de Proxima city en francais"
          longDesc="Premier Servi, use of AI generated assets, ongoing"
          longDescFR="Premier Servi, use of AI generated assets, ongoing"
      />
      <Card
          :img1="BS1"
          :img2="BS2"
          :img3="BS3"
          cardtitle="Barrier Squad" year="2019" v-bind:tags="['Unity', 'Android', 'Tower Defense']"
          desc="Mobile Game, tower defense like, usage of AI generated images"
          descFR="Description de Barrier Squad en francais"
          longDesc="Premier Servi, use of AI generated assets, ongoing"
          longDescFR="Premier Servi, use of AI generated assets, ongoing"
      />
    </div>
  </div>
</template>


<script>
import PS1 from '@/assets/Projects/PS-1.webp';
import PS2 from '@/assets/Projects/PS-2.webp';
import PS3 from '@/assets/Projects/PS-3.webp';

import PC1 from '@/assets/Projects/PC-1.jpg';
import PC2 from '@/assets/Projects/PC-2.jpg';
import PC3 from '@/assets/Projects/PC-3.jpg';

import BS1 from '@/assets/Projects/BS-1.jpg';
import BS2 from '@/assets/Projects/BS-2.jpg';
import BS3 from '@/assets/Projects/BS-3.jpg';

import AV1 from '@/assets/Projects/AV-1.jpg';
// import AV2 from '@/assets/Projects/AV-2.jpg';
// import AV3 from '@/assets/Projects/AV-3.jpg';

import Card from './Card.vue'
import {getCookie} from "@/cookie";

export {}

export default {
  name: 'Projects',
  methods: {getCookie},
  components: {
    Card,
  },
  props: {
    msg: String
  },
  data() {
    return {
      PS1: PS1,
      PS2: PS2,
      PS3: PS3,

      PC1: PC1,
      PC2: PC2,
      PC3: PC3,

      BS1: BS1,
      BS2: BS2,
      BS3: BS3,

      AV1: AV1,
      // AV2: AV2,
      // AV3: AV3,
    }
  },
  mounted() {
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
