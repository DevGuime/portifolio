<template>
  <header>
    <nav>
      <a href="#home" class="brand">Meu Portfólio</a>
      <ul>
        <li><a href="#about">Sobre</a></li>
        <li><a href="#projects">Projetos</a></li>
        <li><a href="#skills">Habilidades</a></li>
        <li><a href="#contact">Contato</a></li>
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
  methods: {
    toggleTheme() {
      this.$emit('toggle-theme');
    }
  }
}
</script>