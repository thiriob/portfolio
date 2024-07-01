<template>
  <div class="container p-0 md:p-10 md:p-2 md:px-20 m-auto">
    <h2 v-if="getCookie('lang') === 'eng'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Game Jam
      Projects</h2>
    <h2 v-if="getCookie('lang') === 'fr'" class="text-3xl mt-6 mb-8 md:mt-10 md:mb-12 text-center">Projets de Game
      Jam</h2>
    <div class="flex flex-wrap justify-center">
      <Card
          :img1="FF"
          :img2="FF2"
          :img3="FF3"
          link="https://lothi.itch.io/ff-xxiv-remake-fraud-fantasy"
          cardtitle="FFXXIV Remake" year="2024" v-bind:tags="['Unity','Narration', 'GGJ']"
          desc="Satire of traditional RPGs."
          descFR="Satyre des RPGS traditionnels."
          longDesc="Achievements: Dialogue system from an easily editable file by the Game Designer. Dialogues adapt to player actions. Worked on 2.5D rendering and player/NPC movements/interactions."
          longDescFR="Réalisations : Système de dialogue depuis un fichier facilement éditable par le Game Designer. 
          Les dialogues s’adaptent aux actions du joueur. Travail sur le rendu 2.5D et les déplacements/intéractions du joueur et des NPC."
      />
      <Card
          video="https://www.youtube.com/embed/yG8GzlaRryQ"
          :img1="FJ"
          :img2="FJ2"
          :img3="FJ3"
          link="https://gaspard-thirion.itch.io/ggj23"
          cardtitle="A fungal journey" year="2023" v-bind:tags="['Unity', 'Exploration', 'GGJ']"
          desc="Adventure game telling the story of a young member of the mushroom tribe."
          descFR="Jeu d'aventure racontant l’histoire d’un jeune habitant de la tribu des champignons."
          longDesc="First 2.5D experience: discovering 2.5D rendering and lighting capabilities in Unity. Created interactions and dialogue systems with NPCs."
          longDescFR="Première expérience en 2.5D : découverte des capacités de rendu et éclairage 2.5d dans Unity. 
          Réalisations des interactions et du système de dialogue avec les NPC."
      />
      <Card
          :img1="JL"
          :img2="JL2"
          :img3="JL3"
          link="https://nonogg.itch.io/jules-achte-du-pain"
          cardtitle="Jules achète du pain" year="2022" v-bind:tags="['Unity', 'Narration', 'GGJ']"
          desc="Narrative experience with multiple choices inviting players to discover all possible scenarios."
          descFR="Expérience narrative à choix multiples invitant à découvrir tous les scénarios possibles."
          longDesc="Created branching system. Display of choices and animations of various scenes."
          longDescFR="Réalisation du système d’embranchement. Affichage des choix et animations des différentes scénettes."
      />
      <Card
          :img1="CH"
          :img2="CH2"
          :img3="CH3"
          link="https://maerys.itch.io/cake-ho"
          cardtitle="Cake Ho!" year="2021" v-bind:tags="['Unity', 'Puzzle', 'MiniJam']"
          desc="Puzzle game set in a pirate universe."
          descFR="Jeu de puzzle dans l’univers des pirates."
          longDesc="Created a simple format allowing the Game Designer to create puzzles without developer intervention. Display and verification of puzzle resolution. Small system allowing the pirate to congratulate the player."
          longDescFR="Création d’un format simple permettant au Game Designer de créer les puzzles sans intervention du développeur.
           Affichage et vérification de la bonne résolution des puzzles. Petit système permettant au pirate de congratuler le joueur."
      />
      <Card
          :img1="LF"
          :img2="LF2"
          link="https://baris-f.itch.io/lost-and-found-office"
          cardtitle="Lost & found office" year="2021" v-bind:tags="['Unity','Puzzle','GGJ']"
          desc="Mini-game that tests the player's observation skills."
          descFR="Mini jeu faisant appel à l’observation du joueur."
          longDesc="Worked on object physics to simulate a disordered pile of items. Random generation of objects. Display of requested items gradually feeding into a simple scoring system."
          longDescFR="Travail sur la physique des objets afin de simuler une pile d’objets désordonnée. Génération des objets de façon aléatoire.
          Affichage des objets demandes au fur et a mesure qui aliment un scoring simple."
      />
      <Card
          :img1="MM"
          :img2="MM2"
          :img3="MM3"
          link="https://florentin-peters.itch.io/miasmaze"
          cardtitle="Miasmaze" year="2020" v-bind:tags="['Unity','Exploration', 'Expressive Jam']"
          desc="Collaborative exploration game."
          descFR="Jeu d’exploration collaboratif."
          longDesc="Created map synchronization between different players via Firebase. Players can also drop messages. Created various static and interactive elements with which Game Designers could build the map."
          longDescFR="Création d’une synchronisation de la map entre les différents joueurs via Firebase. Les joueurs peuvent aussi déposer des messages.
          Réalisations de différents éléments inertes et interactables avec lesquels les Game Designer ont pu créer la map."
      />
    </div>
  </div>
</template>

<script>
import FF from '@/assets/GameJams/FF.jpg';
import FF2 from '@/assets/GameJams/FF2.png';
import FF3 from '@/assets/GameJams/FF3.png';

import FJ from '@/assets/GameJams/FJ.png';
import FJ2 from '@/assets/GameJams/FJ2.jpg';
import FJ3 from '@/assets/GameJams/FJ3.jpg';

import CH from '@/assets/GameJams/CH.jpg';
import CH2 from '@/assets/GameJams/CH2.jpg';
import CH3 from '@/assets/GameJams/CH3.jpg';

import LF from '@/assets/GameJams/LF.png';
import LF2 from '@/assets/GameJams/LF2.png';

import MM from '@/assets/GameJams/MM.png';
import MM2 from '@/assets/GameJams/MM2.png';
import MM3 from '@/assets/GameJams/MM3.png';

import JL from '@/assets/GameJams/JL.png';
import JL2 from '@/assets/GameJams/JL2.png';
import JL3 from '@/assets/GameJams/JL3.jpg';

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
      FF: FF,
      FF2: FF2,
      FF3: FF3,

      FJ: FJ,
      FJ2: FJ2,
      FJ3: FJ3,

      LF: LF,
      LF2: LF2,

      CH: CH,
      CH2: CH2,
      CH3: CH3,

      MM: MM,
      MM2: MM2,
      MM3: MM3,

      JL: JL,
      JL2: JL2,
      JL3: JL3,
    }
  },
  mounted() {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
