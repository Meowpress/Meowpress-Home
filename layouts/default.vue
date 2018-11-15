<template>
  <div>
    <nuxt/>
  </div>
</template>

<style lang="scss">
@import './assets/scss/default.scss';

html {
  // font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
  //   Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  color: #343A40;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--yellow {
  display: inline-block;
  border-radius: 25px;
  border: 1px solid #FF914B;
  color: #FF914B;
  text-decoration: none;
  padding: 10px 40px;
  font-weight: 600;
  margin-left: 15px;
  transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out, border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}

.button--yellow:hover {
  color: #fff;
  background-color: #FF914B;
}

.button--grey {
  display: inline-block;
  border-radius: 25px;
  border: 1px solid #343A40;
  color: #343A40;
  text-decoration: none;
  padding: 10px 40px;
  font-weight: 600;
  transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out, border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}

.button--grey:hover {
  color: #fff;
  background-color: #343A40;
}
</style>
