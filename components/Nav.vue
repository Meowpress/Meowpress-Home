<template>
  <div class="Navbar">
    <b-navbar class="meowpress-navbar" toggleable="md" type="light" variant="light" fixed="top">
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
    <b-navbar-brand tag="h1" class="mb-0">Meowpress</b-navbar-brand>
    <b-collapse is-nav id="nav_collapse">

    <b-navbar-nav>
      <b-link class="to-home" to="/">Home</b-link>
    </b-navbar-nav>
    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto">
      <b-nav-form>
        <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="邀请码"/>
        <b-button class="submit-btn" size="sm" type="submit" variant="dark">注册</b-button>
      </b-nav-form>

      <b-nav-item-dropdown text="Translations" right>
        <b-dropdown-item href="#">English</b-dropdown-item>
        <b-dropdown-item href="#">简体中文</b-dropdown-item>
      </b-nav-item-dropdown>

      <b-nav-item-dropdown right>
        <!-- Using button-content slot -->
        <template slot="button-content">
          User
        </template>
        <b-dropdown-item href="#">Profile</b-dropdown-item>
        <b-dropdown-item href="#">Sign out</b-dropdown-item>
      </b-nav-item-dropdown>
    </b-navbar-nav>
    </b-collapse>
    </b-navbar>
  </div>
</template>

<style>
/* .meowpress-navbar {
  border-top: 3px solid #343A40;
} */
.to-home {
  color: #343A40;
}

.to-home:hover {
  color: #343A40;
}

.navbar-brand {
  font-weight: 600;
}
.submit-btn {
  margin-right: 10px;
}
</style>
