<template>
  <div class="container p-0 md:p-10 md:p-2 md:px-20 m-auto">
    <h2 v-if="getCookie('lang') === 'eng'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Featured
      Projects</h2>
    <h2 v-if="getCookie('lang') === 'fr'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Projets en
      vedette</h2>
    <div class="flex flex-wrap justify-center">
      <Card
          :img1="ST1"
          :img2="ST2"
          :img3="ST3"
          link="https://assetstore.unity.com/preview/288450/937001"
          cardtitle="Scriptable Toolbox" year="2024" v-bind:tags="['Unity','Editor Tool', 'Package']"
          desc="Package published on the Unity asset store."
          descFR="Package publié sur l’asset store de Unity."
          longDesc="Collection of tools intended to help Unity developers working with Scriptable Objects."
          longDescFR="Collection d’outils destinée à aider les développeur Unity travaillant avec les Scriptables Objects."
      />
      <Card
          :img1="PS1"
          :img2="PS2"
          :img3="PS3"
          link="https://gamevrest.com/"
          cardtitle="Premier Servi" year="2023" v-bind:tags="['Unity','Party Game', 'Steam']"
          desc="Colorful hide-and-seek party game inspired by French culture clichés."
          descFR="Party game de cache-cache coloré prenant inspiration des clichés de la culture française."
          longDesc="Planned for Steam release in 2024 and later on Switch. Responsible for the entire technical side, from gameplay and data management to UI logic."
          longDescFR="Objectif de publication sur Steam en 2024 et Switch par la suite.
          Réalisation de toute la partie technique, allant du gameplay à la gestion des données au fonctionnement logique des UI."
      />
      <Card
          video="https://www.youtube.com/embed/o7HDHyE7LWA"
          :img1="AV1"
          :img2="AV2"
          :img3="AV3"
          link="https://www.artstation.com/artwork/qek5eD"
          cardtitle="Aviator" year="2023" v-bind:tags="['Unity', 'Android', 'Firebase', 'Narrative']"
          desc="Narrative experience, applied arts graduation project."
          descFR="Expérience narrative, projet de fin d’études d’arts appliqués."
          longDesc="Implementation: A tablet connected to Firebase controls the main display on a projector. Created a dialogue and cinematic system based on YarnSpinner. Integrated assets created by the client."
          longDescFR="Réalisation : Une tablette connectée à Firebase sert à contrôler l’affichage principal sur un vidéoprojecteur. 
          Création d'un système de dialogue et de cinématique basé sur YarnSpinner.
           Intégration des assets créés par le client."
      />
      <Card
          video="https://www.youtube.com/embed/HJnT_nsFjWY"
          :img1="PC1"
          :img2="PC2"
          :img3="PC3"
          cardtitle="Proxima Cities" year="2020" v-bind:tags="['Unity', 'AR', 'City Builder']"
          desc="AR city builder with an ecological message."
          descFR="City builder AR avec un message écologique."
          longDesc="Implementation of the AR component: visualization of the city and environmental impacts based on player choices. Handled storage and display of various buildings in 2D view along with dynamic roads."
          longDescFR="Réalisation de la partie AR : visualisation de la ville et des impacts sur l’environnement en fonctions des choix du joueur. 
          Je me suis occupé du stockage et affichage des différents bâtiments en vue 2D ainsi que des routes dynamiques."
      />
      <Card
          :img1="BS1"
          :img2="BS2"
          :img3="BS3"
          cardtitle="Barrier Squad" year="2019" v-bind:tags="['Unity', 'Android', 'Tower Defense']"
          desc="Tower defense with original mechanics published on Android."
          descFR="Tower defense avec des mécaniques originales publié sur Android."
          longDesc="Integrated Google Play Games for achievements and high scores, as well as Unity Ads for advertising. Fixed bugs and optimized performance for Android."
          longDescFR="Intégration de Google play games pour les hauts faits et high score ainsi que Unity ads pour la partie publicité. 
          Correction de bugs et optimisations diverses pour améliorer les performances sur Android."
      />
    </div>
  </div>
</template>


<script>
import ST1 from '@/assets/Projects/ST-1.png';
import ST2 from '@/assets/Projects/ST-2.png';
import ST3 from '@/assets/Projects/ST-3.png';

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
import AV2 from '@/assets/Projects/AV-2.jpg';
import AV3 from '@/assets/Projects/AV-3.jpg';

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
      ST1: ST1,
      ST2: ST2,
      ST3: ST3,

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
      AV2: AV2,
      AV3: AV3,
    }
  },
  mounted() {
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
