<template>
  <div class="container m-auto p-4 px-4 md:p-10 md:p-2 md:px-20">
    <div class="flex flex-col">
      <div class="flex flex-wrap mt-14 md:mt-0">
        <div class="md:w-1/2 w-full m-auto">
          <img class="rounded-full m-auto md:h-80 md:w-80 h-52 w-52 object-cover" src="@/assets/photo.jpeg"
               alt="Picture of Gaspard thirion">
        </div>
        <div class="md:w-1/2 md:p-0 sm:p-4 flex flex-col">
          <div class="flex-grow mt-4">
            <h1 class="text-4xl">{{ msg }}</h1>
            <h2 class="text-2xl ml-2 mt-2 md:mt-5" v-if="getCookie('lang') === 'eng'">C# Developer </h2>
            <h2 class="text-2xl ml-2 mt-2 md:mt-5" v-if="getCookie('lang') === 'fr'">Développeur C#</h2>
            <p v-if="getCookie('lang') === 'eng'" class="ml-2 sm:py-3 pt-1">
              Developer from a young age, I made a career out of it when I graduated from Epitech.
              <br> I am currently diversifying my skill set.
              <br>C# is the language I have the most expertise in, allowing me to explore other technologies such as
              WPF, Avalonia, ASP...
              <br>Numerous GameJam experiences have enabled me to become versatile, efficient in my developments and
              able to quickly adapt to a new team.
              <br> I'm also a national-level Biketrial competitor.
            </p>
            <p v-if="getCookie('lang') === 'fr'" class="ml-2 sm:py-3 pt-1 md:text-base text-sm">
              Développeur Unity depuis toujours, j'en ai fait mon métier à la fin de mes études à Epitech.
              <br>Je diversifie désormais mes compétences.
              <br>Le C# est mon langage le plus approfondi et me permets d'approcher d'autres technologies comme WPF,
              Avalonia, Asp...
              <br>De nombreuses expériences de GameJam m'ont permis de devenir polyvalent, d'être efficace dans mes
              développements et de m'adapter rapidement à une nouvelle équipe.
              <br>Je suis en parallèle compétiteur de niveau national en Biketrial.
            </p>
          </div>
          <div class="mt-2 space-x-1 sm:space-x-3">
            <!-- todo translate and add english CV -->
            <a v-if="getCookie('lang') === 'eng'" href="CV_Gaspard_Thirion_2024_FR_csharp.pdf" target="_blank"
               rel="noreferrer">
              <button class="bg-celadonBlue hover:bg-prussianBlue">
                <svg class="sm:w-5 sm:w-5 w-4 h-4 fill-current" role="img" viewBox="0 0 42 42"
                     xmlns="http://www.w3.org/2000/svg">
                  <g>
                    <path
                        d="M34.395,0H9.522c-2.762,0-5,2.239-5,5v33.916c0,2.761,2.238,5,5,5h24.871c2.762,0,5-2.239,5-5V5C39.395,2.239,37.154,0,34.395,0z M9.208,16.855c0-1.172,0.951-2.121,2.121-2.121h0.742c-0.791-0.874-1.277-2.03-1.277-3.304c0-2.723,2.209-4.931,4.932-4.931c2.725,0,4.932,2.207,4.932,4.932c0,1.272-0.486,2.429-1.279,3.303h0.709c1.172,0,2.121,0.949,2.121,2.121v3.578c0,1.122-0.875,2.03-1.975,2.106h-9.051c-1.1-0.076-1.975-0.984-1.975-2.106V16.855L9.208,16.855z M32.708,37.416h-21.5c-1.104,0-2-0.896-2-2s0.896-2,2-2h21.5c1.104,0,2,0.896,2,2S33.812,37.416,32.708,37.416zM32.708,29.916h-21.5c-1.104,0-2-0.896-2-2s0.896-2,2-2h21.5c1.104,0,2,0.896,2,2S33.812,29.916,32.708,29.916zM32.708,22.416 h-6.5c-1.104,0-2-0.896-2-2c0-1.104,0.896-2,2-2h6.5c1.104,0,2,0.896,2,2C34.708,21.52,33.812,22.416,32.708,22.416z"/>
                  </g>
                </svg>
                <span class="xl:hidden">Resume</span><span class="xl:block hidden">View Resume</span>
              </button>
            </a>
            <a v-if="getCookie('lang') === 'fr'" href="CV_Gaspard_Thirion_2024_FR_csharp.pdf" target="_blank"
               rel="noreferrer">
              <button class="bg-celadonBlue hover:bg-prussianBlue">
                <svg class="sm:w-5 sm:w-5 w-4 h-4 fill-current" role="img" viewBox="0 0 42 42"
                     xmlns="http://www.w3.org/2000/svg">
                  <g>
                    <path
                        d="M34.395,0H9.522c-2.762,0-5,2.239-5,5v33.916c0,2.761,2.238,5,5,5h24.871c2.762,0,5-2.239,5-5V5C39.395,2.239,37.154,0,34.395,0z M9.208,16.855c0-1.172,0.951-2.121,2.121-2.121h0.742c-0.791-0.874-1.277-2.03-1.277-3.304c0-2.723,2.209-4.931,4.932-4.931c2.725,0,4.932,2.207,4.932,4.932c0,1.272-0.486,2.429-1.279,3.303h0.709c1.172,0,2.121,0.949,2.121,2.121v3.578c0,1.122-0.875,2.03-1.975,2.106h-9.051c-1.1-0.076-1.975-0.984-1.975-2.106V16.855L9.208,16.855z M32.708,37.416h-21.5c-1.104,0-2-0.896-2-2s0.896-2,2-2h21.5c1.104,0,2,0.896,2,2S33.812,37.416,32.708,37.416zM32.708,29.916h-21.5c-1.104,0-2-0.896-2-2s0.896-2,2-2h21.5c1.104,0,2,0.896,2,2S33.812,29.916,32.708,29.916zM32.708,22.416 h-6.5c-1.104,0-2-0.896-2-2c0-1.104,0.896-2,2-2h6.5c1.104,0,2,0.896,2,2C34.708,21.52,33.812,22.416,32.708,22.416z"/>
                  </g>
                </svg>
                <span class="sm:hidden">CV</span><span class="sm:block hidden">Voir mon CV</span>
              </button>
            </a>
            <a href="https://linkedin.com/in/gaspard-thirion">
              <button class="h-10 bg-celadonBlue hover:bg-prussianBlue">
                <svg class="sm:w-5 sm:w-5 w-4 h-4  fill-current" role="img" viewBox="0 0 256 256"
                     xmlns="http://www.w3.org/2000/svg">
                  <g>
                    <path
                        d="M218.123122,218.127392 L180.191928,218.127392 L180.191928,158.724263 C180.191928,144.559023 179.939053,126.323993 160.463756,126.323993 C140.707926,126.323993 137.685284,141.757585 137.685284,157.692986 L137.685284,218.123441 L99.7540894,218.123441 L99.7540894,95.9665207 L136.168036,95.9665207 L136.168036,112.660562 L136.677736,112.660562 C144.102746,99.9650027 157.908637,92.3824528 172.605689,92.9280076 C211.050535,92.9280076 218.138927,118.216023 218.138927,151.114151 L218.123122,218.127392 Z M56.9550587,79.2685282 C44.7981969,79.2707099 34.9413443,69.4171797 34.9391618,57.260052 C34.93698,45.1029244 44.7902948,35.2458562 56.9471566,35.2436736 C69.1040185,35.2414916 78.9608713,45.0950217 78.963054,57.2521493 C78.9641017,63.090208 76.6459976,68.6895714 72.5186979,72.8184433 C68.3913982,76.9473153 62.7929898,79.26748 56.9550587,79.2685282 M75.9206558,218.127392 L37.94995,218.127392 L37.94995,95.9665207 L75.9206558,95.9665207 L75.9206558,218.127392 Z M237.033403,0.0182577091 L18.8895249,0.0182577091 C8.57959469,-0.0980923971 0.124827038,8.16056231 -0.001,18.4706066 L-0.001,237.524091 C0.120519052,247.839103 8.57460631,256.105934 18.8895249,255.9977 L237.033403,255.9977 C247.368728,256.125818 255.855922,247.859464 255.999,237.524091 L255.999,18.4548016 C255.851624,8.12438979 247.363742,-0.133792868 237.033403,0.000790807055">
                    </path>
                  </g>
                </svg>
                <span class="xl:block hidden">Linkedin</span>
              </button>
            </a>
            <Mailto mail="gaspard.thirion@gmail.com" target="_blank">
              <button class="h-10 bg-celadonBlue hover:bg-prussianBlue">
                <svg class="sm:w-5 sm:w-5 w-4 h-4  fill-current" role="img" viewBox="0 4 30 25"
                     xmlns="http://www.w3.org/2000/svg">
                  <path
                      d="m3 8v18h26v-18zm4.3125 2h17.375l-8.6875 5.7812zm-2.3125.875 10.4375 6.9688.5625.3437.5625-.3437 10.4375-6.9688v13.125h-22z"/>
                </svg>
                <span class="xl:block hidden">Mail</span>
              </button>
            </Mailto>
          </div>
        </div>
      </div>
    </div>

  </div>

</template>

<script>
import {getCookie} from "../cookie";
import Mailto from "@/components/Mailto.vue";
/*
I am 25 French Programmer that is very curious for new technologies and interested in every aspect of a project from design to delivery, as well as business and project management.
I am looking into joining an interested project and meet people working on interesting topics in my plan to establish myself in Korea !

 */
export default {
  name: 'About',
  components: {Mailto},
  props: {
    msg: String
  },
  methods: {
    getCookie
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
