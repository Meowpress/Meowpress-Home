<template>
<div>
  <Nav/>
  <section class="container">
    <div>
      <h1 class="title">
        <i class="fa fa-tags"></i> Login
      </h1>
      <h2 class="subtitle">
        Meow, yet another open source blogging platform.
      </h2>
      <div class="login">
    <b-form @submit="onSubmit" v-if="show">
      <b-form-group id="userEmail"
                    label="Email address:"
                    label-for="userEmailLabel"
                    description="We'll never share your email with anyone else.">
        <b-form-input id="userEmailLabel"
                      type="email"
                      v-model="form.email"
                      required
                      placeholder="Enter email">
        </b-form-input>
      </b-form-group>
      <b-form-group id="userName"
                    label="Your Name:"
                    label-for="userNameLabel">
        <b-form-input id="userNameLabel"
                      type="text"
                      v-model="form.name"
                      required
                      placeholder="Enter name">
        </b-form-input>
      </b-form-group>
      <b-form-group id="userTheme"
                    label="Theme:"
                    label-for="userThemeLabel">
        <b-form-select id="userThemeLabel"
                      :options="foods"
                      required
                      v-model="form.food">
        </b-form-select>
      </b-form-group>
      <b-form-group id="exampleGroup4">
        <b-form-checkbox-group v-model="form.checked" id="exampleChecks">
          <b-form-checkbox value="me">Check me out</b-form-checkbox>
          <b-form-checkbox value="that">Check that out</b-form-checkbox>
        </b-form-checkbox-group>
      </b-form-group>
      <b-button type="submit" variant="dark">Submit</b-button>
    </b-form>
    <div>
  </div>
      </div>
    </div>
  </section>
  <div class="footer">
    Follow us on
    <a href="#foo"><i class="fa fa-github" aria-hidden="true"></i> GitHub</a> · 
    <a href="#foo"><i class="fa fa-telegram" aria-hidden="true"></i> Telegram</a> · 
    <a href="#foo"><i class="fa fa-weibo" aria-hidden="true"></i> Weibo</a> and more.<br>
    ©2018 Proudly made with <i class="fa fa-heart" aria-hidden="true"></i> from BIT.
  </div>
</div>
</template>

<script>
import Nav from '~/components/Nav.vue'

export default {
  components: {
    Nav
  },
  data() {
    return {
      form: {
        email: '',
        name: '',
        food: null,
        checked: []
      },
      foods: [
        { text: 'Select One', value: null },
        'Carrots',
        'Beans',
        'Tomatoes',
        'Corn'
      ],
      show: true
    }
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault()
      alert(JSON.stringify(this.form))
    }
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
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 600;
  font-size: 64px;
  color: #343a40;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 32px;
  color: #343a40;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.main-button-text {
  padding: 6px 0;
}

.intro-container-1,
.intro-container-2,
.intro-container-3 {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.intro-container-1,
.intro-container-3 {
  background-color: #fafafa;
}

.footer {
  padding: 3rem;
  text-align: center;
  color: #fff;
  text-decoration: none;
  background-color: #343a40;
  line-height: 2rem;
}

a {
  text-decoration: none;
  color: #fafafa;
}

a:hover {
  color: #fafafa;
}
</style>
