<template>
<div>
  <Nav/>
  <section class="container">
    <div class="signup-wrapper">
      <h1 class="title">
        <i class="fa fa-tags"></i> Sign up
      </h1>
      <h2 class="subtitle">
        Meow, yet another open source blogging platform.
      </h2>
      <div class="signup">
        <b-form @submit="onSubmit" v-if="show">
            <b-form-group id="userName"
                        label="Your Name:"
                        label-for="userNameLabel"
                        description="Let us know your name!">
            <b-form-input id="userNameLabel"
                          type="text"
                          v-model="form.name"
                          required
                          placeholder="Enter name">
            </b-form-input>
          </b-form-group>
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
                    <b-form-group id="userPassword"
                        label="Password:"
                        label-for="userPasswordLabel"
                        description="Create a strong and secure password.">
            <b-form-input id="userPasswordLabel"
                          type="password"
                          v-model="form.password"
                          required
                          placeholder="Create a password">
            </b-form-input>
          </b-form-group>
          <!-- <b-form-group id="userTheme"
                        label="Theme:"
                        label-for="userThemeLabel">
            <b-form-select id="userThemeLabel"
                          :options="foods"
                          required
                          v-model="form.food">
            </b-form-select>
          </b-form-group> -->
          <b-form-group id="exampleGroup4">
            <b-form-checkbox-group v-model="form.checked" id="exampleChecks">
              <b-form-checkbox value="me">Check me out</b-form-checkbox>
              <b-form-checkbox value="that">Check that out</b-form-checkbox>
            </b-form-checkbox-group>
          </b-form-group>
          <b-button type="submit" variant="dark">Submit</b-button>
        </b-form>
      </div>
    </div>
  </section>
  <Footer/>
</div>
</template>

<script>
import Nav from '~/components/Nav.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Nav,
    Footer
  },
  data() {
    return {
      form: {
        email: '',
        name: '',
        checked: []
      },
      // foods: [
      //   { text: 'Select One', value: null },
      //   'Carrots',
      //   'Beans',
      //   'Tomatoes',
      //   'Corn'
      // ],
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
  /* font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif; */
  font-family: 'Merriweather', serif;
  display: block;
  font-weight: 900;
  font-size: 64px;
  color: #343a40;
  letter-spacing: 1px;
}

.subtitle {
  font-family: 'Montserrat', serif;
  font-weight: 400;
  font-size: 32px;
  color: #343a40;
  word-spacing: 1px;
  padding-bottom: 15px;
}

.signup-wrapper {
  max-width: 600px;
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
  color: #FAFAFA;
}

a:hover {
  color: #FAFAFA;
}
</style>
