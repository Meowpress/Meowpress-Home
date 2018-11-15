<template>
<div>
  <Nav/>
  <section class="container">
    <div>
      <Logo/>
      <h1 class="title">
        Meowpress
      </h1>
      <h2 class="subtitle">
        Meow, yet another open source blogging platform.
      </h2>
      <div class="links">
        <a
          href="https://github.com/Meowpress"
          target="_blank"
          class="button--grey">GitHub</a>
        <nuxt-link
          to="/signup"
          class="button--yellow">Sign up</nuxt-link>
      </div>
    </div>
  </section>
  <section class="intro-container-1">
    <h2>
      顺滑、Markdown 友好的博客体验
    </h2>
  </section>
  <section class="intro-container-2">
    <h2>
      精致、编辑精选的免费主题
    </h2>
  </section>
  <section class="intro-container-3">
    <h2>
      五分钟迅捷建站
    </h2>
  </section>
  <Footer/>
</div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Nav from '~/components/Nav.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Logo,
    Nav,
    Footer
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: left;
}

.title {
  /* font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif; */
  font-family: 'Merriweather', serif;
  display: block;
  font-weight: 900;
  font-size: 64px;
  color: #343A40;
  letter-spacing: 1px;
  padding-top: 2rem;
}

.subtitle {
  font-family: 'Montserrat', serif;
  font-weight: 400;
  font-size: 32px;
  color: #343A40;
  word-spacing: 1px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.main-button-text {
  padding: 6px 0;
}

.intro-container-1, .intro-container-2, .intro-container-3 {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.intro-container-1, .intro-container-3 {
  background-color: #FAFAFA;
}

a {
  text-decoration: none;
  color: #FAFAFA;
}

a:hover {
  color: #FAFAFA;
}
</style>
