<template>
  <div class="Navbar">
    <b-navbar class="meowpress-navbar" toggleable="md" type="light" variant="light" fixed="top">
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
    <b-navbar-brand tag="h1" class="mb-0">Meowpress</b-navbar-brand>
    <b-collapse is-nav id="nav_collapse">

    <b-navbar-nav>
      <b-link class="nav-link" to="/">Home</b-link>
    </b-navbar-nav>
    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto">
      <b-nav-item>
        <b-badge class="nav-brand-badge" variant="primary">v1.0.0</b-badge>
      </b-nav-item>
      <b-nav-item href="https://github.com/Meowpress"> <i class="fa fa-github" aria-hidden="true"></i> GitHub </b-nav-item>
      <b-nav-item href="/"> <i class="fa fa-slack" aria-hidden="true"></i> Slack </b-nav-item>
      <b-nav-item href="/"> <i class="fa fa-telegram" aria-hidden="true"></i> Telegram </b-nav-item>
      <!-- <b-nav-form>
        <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="邀请码"/>
      </b-nav-form> -->
      <!-- <b-button class="submit-btn" size="sm" type="submit" variant="dark">登录</b-button> -->
      <b-nav-item-dropdown text="Translations" right>
        <b-dropdown-item href="#">English</b-dropdown-item>
        <b-dropdown-item href="#">简体中文</b-dropdown-item>
      </b-nav-item-dropdown>
      <b-nav-item> | </b-nav-item>
      <b-link class="nav-link" to="/login">Login</b-link>

    </b-navbar-nav>
    </b-collapse>
    </b-navbar>
  </div>
</template>

<style>
/* .meowpress-navbar {
  border-top: 3px solid #343A40;
} */
.nav-brand-badge {
  color: #ffffff;
  font-weight: 400;
}
.nav-link {
  color: #343A40;
}

.nav-link:hover {
  color: #343A40;
}

.navbar-brand {
  font-weight: 600;
}
/* .submit-btn {
  margin-right: 10px;
  padding: 2px 20px;
} */
</style>
