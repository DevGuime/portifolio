<template>
  <div id="app" :class="theme">
    <Header :theme="theme" @toggle-theme="toggleTheme" />
    <main>
      <Home />
      <About />
      <Projects />
      <Skills />
      <Contact />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Home from './components/Home.vue'
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Home,
    About,
    Projects,
    Skills,
    Contact,
    Footer
  },
  data() {
    return {
      theme: 'dark'
    }
  },
  methods: {
    toggleTheme() {
      this.theme = this.theme === 'dark' ? 'light' : 'dark';
    }
  }
}
</script>

<style>
/* Styles are now in src/assets/main.css */
</style>