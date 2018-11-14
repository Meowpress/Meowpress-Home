<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        Meowpress
      </h1>
      <h2 class="subtitle">
        Meow, yet another open source blogging platform.
      </h2>
      <div class="links">
        <!-- <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green">Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey">GitHub</a> -->
        <b-button href="#" size="lg" variant="primary">
          即刻开始 →
        </b-button>
        <b-button href="https://github.com/nuxt/nuxt.js" size="lg" variant="primary">
          GitHub
        </b-button>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 600;
  font-size: 64px;
  color: #2c2c2c;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 32px;
  color: #2c2c2c;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
