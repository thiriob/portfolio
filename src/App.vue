<template>
  <div id="app" class="h-screen light">
    <Nav/>
    <section id="about" class="flex h-full max-h-screen overflow-y-auto">
      <About msg="Gaspard Thirion"/>
      <Arrow/>
    </section>
    <section id="projects" class="flex w-full">
      <Projects msg="Gaspard Thirion"/>
    </section>
    <section id="projectsGJ" class="flex w-full">
      <ProjectsGJ msg="Gaspard Thirion"/>
    </section>
    <section id="contact" class="flex w-full">
      <ContactMe/>
    </section>
  </div>
</template>

<script>
import Nav from './components/Nav.vue'
import About from './components/About.vue'
import Projects from '@/components/Projects.vue'
import ProjectsGJ from '@/components/ProjectsGJ.vue'
import Arrow from '@/components/Arrow.vue'
import ContactMe from "@/components/ContactMe.vue";
import {setCookie} from "./cookie";

export default {
  name: 'App',
  components: {
    ContactMe,
    Nav,
    About,
    Arrow,
    Projects,
    ProjectsGJ,
  },
  data() {
    return {
      lang: "eng"
    }
  },
  mounted() {
    setCookie("lang", 'fr', 1000)
  },
}

</script>

<style>

</style>
