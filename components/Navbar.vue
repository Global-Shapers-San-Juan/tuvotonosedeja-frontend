<template>
  <div class="navbar-margin">
    <b-navbar toggleable="lg" variant="danger" type="dark" fixed="top">
      <b-navbar-brand href="/">
        <img
          src="~/assets/logo.png"
          alt="Tu Voto No se Deja Logo"
          class="navbar-logo"
        />
        Conoce tus Candidatxs
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="/">Info</b-nav-item>
          <b-nav-item href="/gobernacion">Gobernacion</b-nav-item>
          <b-nav-item href="/senado">Senado</b-nav-item>
          <b-nav-item href="/representantes">Representantes</b-nav-item>

          <b-nav-form class="ml-3">
            <b-form-input
              size="sm"
              class="mr-sm-2"
              placeholder="Search"
            ></b-form-input>
            <b-button
              size="sm"
              class="my-2 my-sm-0"
              type="submit"
              variant="outline-light"
              >Search</b-button
            >
          </b-nav-form>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<style>
.navbar-logo {
  height: 48px;
}
/* .navbar-collapse.collapse.show {
  height: 100vh;
} */
.navbar-toggler {
  padding: 0px;
}
.navbar-margin {
  margin-bottom: 72px;
}
</style>
