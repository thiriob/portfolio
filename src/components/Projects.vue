<template>
  <div class="container p-0 md:p-10 md:p-2 md:px-20 m-auto">
    <h2 v-if="getCookie('lang') === 'eng'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Featured Projects</h2>
    <h2 v-if="getCookie('lang') === 'kr'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">특징 프로젝트</h2>
    <div class="flex flex-wrap justify-center">
      <Card :img="PR" link="https://gamevrest.odoo.com/" cardtitle="Premier Servi" year="2023" v-bind:tags="['Unity', 'Content creation', 'AI']"
            desc="Premier Servi, use of AI generated assets, ongoing"
            descKR="Premier Servi, AI 생성 자산의 사용, 지속적인"/>
      <Card :img="Proxima" link="https://play.google.com/store/apps/details?id=com.gamevrest.proximaCities" cardtitle="Proxima Cities" year="2020" v-bind:tags="['Unity', 'C#']"
            desc="Augmented reality city, on mobile application"
            descKR="모바일 애플리케이션상의 증강현실 도시"/>
      <Card :img="BR" link="https://play.google.com/store/apps/details?id=com.InDustry.BarriersQuad&hl=en&gl=US" cardtitle="Barrier Squad" year="2019" v-bind:tags="['Unity', 'Android']"
            desc="Mobile Game, tower defense like, usage of AI generated images"
            descKR="모바일 게임, 타워 방어 같은 것"/>
    </div>
  </div>
</template>


<script>
import Card from './Card.vue'
import {getCookie} from "@/cookie";
import PR from '@/assets/PremierServi.png';
import Proxima from '@/assets/Proxima.png';
import BR from '@/assets/BarrierSquad.png';

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
  data(){
    return {
      PR : PR,
      Proxima : Proxima,
      BR : BR,
    }
  },
  mounted(){
    //this.PR = PR.toString();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
