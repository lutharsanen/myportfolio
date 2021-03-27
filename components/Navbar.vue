<template>
<div>
  <div class="desktop">
   <div>
      <b-navbar type="dark" variant="dark">
        <b-navbar-nav>
          <b-nav-item href="#">Home</b-nav-item>

          <!-- Navbar dropdowns -->
          <b-nav-item-dropdown text="About" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown text="User" right>
            <b-dropdown-item href="#">Account</b-dropdown-item>
            <b-dropdown-item href="#">Settings</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-navbar>
    </div>
  </div>

  <div class="mobile">
    <b-navbar toggleable type="dark" variant="dark">
      <b-navbar-brand href="#">LK</b-navbar-brand>

      <b-navbar-toggle target="navbar-toggle-collapse">
        <template #default="{ expanded }">
          <b-icon v-if="expanded" icon="chevron-bar-up"></b-icon>
          <b-icon v-else icon="chevron-bar-down"></b-icon>
        </template>
      </b-navbar-toggle>

      <b-collapse id="navbar-toggle-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#">Link 1</b-nav-item>
          <b-nav-item href="#">Link 2</b-nav-item>
          <b-nav-item href="#" disabled>Disabled</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>

  </div>
</template>

<style>
  .mobile{
    display: None;
  }

  .b-navbar{
    background-color: black;
  }

@media only screen and (max-width: 768px) {
  .desktop{
    display: None;
  }

  .mobile{
    display: block;
  }
  
}

</style>
