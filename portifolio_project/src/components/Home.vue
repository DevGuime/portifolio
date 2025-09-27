<template>
  <section id="home" class="hero">
    <div class="hero-text">
      <h1>Olá, me chamo Guilherme</h1>
      <p>Eu sou <span class="typing">{{ typedText }}</span></p>
      <a href="#projects" class="btn">Veja meus projetos</a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      roles: ["Desenvolvedor Web", "Entusiasta de IA", "Engenheiro de Software"],
      currentRoleIndex: 0,
      typedText: "",
      isDeleting: false,
      typingSpeed: 100,
      deletingSpeed: 50,
      delay: 2000,
    };
  },
  mounted() {
    this.type();
  },
  methods: {
    type() {
      const currentRole = this.roles[this.currentRoleIndex];
      if (this.isDeleting) {
        this.typedText = currentRole.substring(0, this.typedText.length - 1);
      } else {
        this.typedText = currentRole.substring(0, this.typedText.length + 1);
      }

      let typeSpeed = this.isDeleting ? this.deletingSpeed : this.typingSpeed;

      if (!this.isDeleting && this.typedText === currentRole) {
        typeSpeed = this.delay;
        this.isDeleting = true;
      } else if (this.isDeleting && this.typedText === "") {
        this.isDeleting = false;
        this.currentRoleIndex = (this.currentRoleIndex + 1) % this.roles.length;
      }

      setTimeout(this.type, typeSpeed);
    },
  },
};
</script>

<style scoped>
.typing {
  border-right: 2px solid;
  animation: blink 0.7s steps(1) infinite;
}

@keyframes blink {
  50% {
    border-color: transparent;
  }
}
</style>