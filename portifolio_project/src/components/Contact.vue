<template>
  <section id="contact">
    <h2>Entre em Contato</h2>
    <p>Sinta-se à vontade para me contatar para colaborações ou apenas para dizer um olá!</p>
    <div class="contact-container">
        <form>
          <input type="text" placeholder="Seu Nome">
          <input type="email" placeholder="Seu Email">
          <textarea placeholder="Sua Mensagem"></textarea>
          <button type="submit" class="btn">Enviar Mensagem</button>
        </form>
        <div class="social-links">
            <h3>Minhas Redes</h3>
            <a href="https://github.com/DevGuime" target="_blank"><i class="devicon-github-original"></i> GitHub</a>
            <a href="https://www.linkedin.com/in/guilherme-sim%C3%B5es-293277186/" target="_blank"><i class="devicon-linkedin-plain"></i> LinkedIn</a>
        </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Contact'
}
</script>