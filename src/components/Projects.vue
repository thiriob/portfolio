<template>
  <div class="container p-0 md:p-10 md:p-2 md:px-20 m-auto">
    <h2 v-if="getCookie('lang') === 'eng'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Featured
      Projects</h2>
    <h2 v-if="getCookie('lang') === 'fr'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Projets en
      vedette</h2>
    <div class="flex flex-wrap justify-center">
      <Card :img="PR" link="https://gamevrest.odoo.com/"
            cardtitle="Premier Servi" year="2023" v-bind:tags="['Unity','Party Game', 'Steam']"
            desc="Premier Servi, use of AI generated assets, ongoing"
            descFR="Description de Premier servi en francais"
            longDesc="Long description for Premier servi"
            longDescFR="Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi Description longue pour premier servi"
      />
      <Card :img="Proxima" link="https://play.google.com/store/apps/details?id=com.gamevrest.proximaCities"
            cardtitle="Proxima Cities" year="2020" v-bind:tags="['Unity', 'AR', 'City Builder']"
            desc="Augmented reality city, on mobile application"
            descFR="Description de Proxima city en francais"
            longDesc="Premier Servi, use of AI generated assets, ongoing"
            longDescFR="Premier Servi, use of AI generated assets, ongoing"
      />
      <Card :img="BR" link="https://play.google.com/store/apps/details?id=com.InDustry.BarriersQuad&hl=en&gl=US"
            cardtitle="Barrier Squad" year="2019" v-bind:tags="['Unity', 'Android', 'Tower Defense']"
            desc="Mobile Game, tower defense like, usage of AI generated images"
            descFR="Description de Barrier Squad en francais"
            longDesc="Premier Servi, use of AI generated assets, ongoing"
            longDescFR="Premier Servi, use of AI generated assets, ongoing"
      />
      <Card :img="Aviator" link="https://play.google.com/store/apps/details?id=com.InDustry.BarriersQuad&hl=en&gl=US"
            cardtitle="Aviator" year="2023" v-bind:tags="['Unity', 'Android', 'Firebase', 'Narrative']"
            desc="Mobile Game, tower defense like, usage of AI generated images"
            descFR="Description de Aviator en francais"
            longDesc="Premier Servi, use of AI generated assets, ongoing"
            longDescFR="Premier Servi, use of AI generated assets, ongoing"
      />
    </div>
  </div>
</template>


<script>
import Card from './Card.vue'
import {getCookie} from "@/cookie";
import PR from '@/assets/PremierServi.png';
import Proxima from '@/assets/Proxima.png';
import BR from '@/assets/BarrierSquad.png';
import Aviator from '@/assets/BarrierSquad.png';

console.log(PR.toString());
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
      PR: PR,
      Proxima: Proxima,
      BR: BR,
      Aviator: Aviator,
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
