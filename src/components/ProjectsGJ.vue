<template>
  <div class="container p-0 md:p-10 md:p-2 md:px-20 m-auto">
    <h2 v-if="getCookie('lang') === 'eng'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Game Jam
      Projects</h2>
    <h2 v-if="getCookie('lang') === 'fr'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Projets de Game
      Jam</h2>
    <div class="flex flex-wrap justify-center">
      <Card :img1= "PR"
            img2= "PR"
            img3= "PR"
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
import Card from './Card.vue'
import {getCookie} from "@/cookie";
import PR from '@/assets/PremierServi.png';
import Proxima from '@/assets/Proxima.png';
import BR from '@/assets/BarrierSquad.png';
import Aviator from '@/assets/BarrierSquad.png';

console.log(PR.toString());
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
