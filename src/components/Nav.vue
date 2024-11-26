<template>
  <nav class="fixed w-full bg-cultured z-10">
    <div
        class="container flex justify-start md:justify-center items-center p-5 mx-auto text-gray-800 capitalize dark:text-gray-300">
      <div>
        <a href="#about"
           class="border-b-2 border-transparent hover:text-gray-900 dark:hover:text-gray-200 hover:border-celadonBlue mx-1.5 sm:mx-6">About</a>
        <a href="#projects"
           class="border-b-2 border-transparent hover:text-gray-900 dark:hover:text-gray-200 hover:border-celadonBlue mx-1.5 sm:mx-6">Projects</a>
        <a href="#projectsGJ"
           class="hidden md:inline border-b-2 border-transparent hover:text-gray-900 dark:hover:text-gray-200 hover:border-celadonBlue mx-1.5 sm:mx-6">Game
          Jams</a>
        <a href="#contact"
           class="border-b-2 border-transparent hover:text-gray-900 dark:hover:text-gray-200 hover:border-celadonBlue mx-1.5 sm:mx-6">Contact</a>
      </div>
<!--      <div class="container absolute flex justify-end pointer-events-none">-->
<!--&lt;!&ndash;        <div class="pointer-events-auto flex mr-8">&ndash;&gt;-->
<!--&lt;!&ndash;          <img @click="changeLang('fr')"&ndash;&gt;-->
<!--&lt;!&ndash;               src="@/assets/france.png"&ndash;&gt;-->
<!--&lt;!&ndash;               alt="france"&ndash;&gt;-->
<!--&lt;!&ndash;               class="w-8 cursor-pointer mr-2"&ndash;&gt;-->
<!--&lt;!&ndash;          />&ndash;&gt;-->
<!--&lt;!&ndash;          <img @click="changeLang('eng')"&ndash;&gt;-->
<!--&lt;!&ndash;               src="@/assets/united-kingdom.png"&ndash;&gt;-->
<!--&lt;!&ndash;               alt="united-kingdom"&ndash;&gt;-->
<!--&lt;!&ndash;               class="w-8 cursor-pointer"&ndash;&gt;-->
<!--&lt;!&ndash;          />&ndash;&gt;-->
<!--        </div>-->
<!--      </div>-->
    </div>
  </nav>
</template>

<script>
import {setCookie} from "../cookie";

import franceFlag from '@/assets/france.png'

export default {
  name: 'Nav',
  methods: {
    changeLang(lang) {
      setCookie("lang", lang, 1000)
      location.reload();
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

a {
  @apply text-black;
}
</style>
