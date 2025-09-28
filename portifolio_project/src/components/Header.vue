<template>
  <header>
    <nav>
      <a href="#home" class="brand">Meu Portfólio</a>
      <div class="menu-toggle" @click="toggleMenu">
        <i class="fas fa-bars"></i>
      </div>
      <ul :class="{ 'nav-active': isMenuOpen }">
        <li><a href="#about" @click="closeMenu">Sobre</a></li>
        <li><a href="#projects" @click="closeMenu">Projetos</a></li>
        <li><a href="#skills" @click="closeMenu">Habilidades</a></li>
        <li><a href="#contact" @click="closeMenu">Contato</a></li>
        <li>
          <button @click="toggleTheme" class="theme-switcher">
            <i v-if="theme === 'dark'" class="fas fa-sun"></i>
            <i v-else class="fas fa-moon"></i>
          </button>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: ['theme'],
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
    toggleTheme() {
      this.$emit('toggle-theme');
    },
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    closeMenu() {
      this.isMenuOpen = false;
    }
  }
}
</script>