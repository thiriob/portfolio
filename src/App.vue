<template>
  <div id="app" class="h-screen light">
    <Nav/>
    <section id="about" class="flex h-full">
      <About msg="Gaspard Thirion"/>
      <Arrow/>
    </section>
    <a class="anchor" id="agile"></a>
    <section id="projects" class="flex w-full">
      <Projects msg="Gaspard Thirion"/>
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
import Arrow from '@/components/Arrow.vue'
import ContactMe from "@/components/ContactMe.vue";

export default {
  name: 'App',
  components: {
    ContactMe,
    Nav,
    About,
    Arrow,
    Projects,
  },
  data() {
    return {
      lang: "eng"
    }
  }
}
</script>

<style>

</style>
