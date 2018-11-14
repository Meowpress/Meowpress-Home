<template>
  <div class="Navbar">
    <b-navbar toggleable="md" type="light" variant="faded" fixed="top">
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
    <b-navbar-brand tag="h1" class="mb-0">Meowpress</b-navbar-brand>
    <b-collapse is-nav id="nav_collapse">

    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto">
      <b-nav-form>
        <b-form-input size="sm" class="mr-sm-2" type="text" placeholder="Email"/>
        <b-button size="sm" class="submit-email" variant="dark">Sign in</b-button>
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
.Meowpress-nav-logo {
  margin-right: 10px;
}
</style>
