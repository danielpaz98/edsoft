<template>
  <div>
    <span
      id="nav-menu-open-btn"
      class="jam jam-menu"
      @click="toggleMenu()"
    ></span>

    <nav
      id="nav-menu"
      :class="{ show: openMenu }"
      class="nav-menu"
      ref="navMenu"
    >
      <span
        id="nav-menu-close-btn"
        class="jam jam-close"
        @click="toggleMenu()"
      ></span>

      <ul class="main-menu">
        <li class="main-menu-item">
          <nuxt-link to="/">Inicio</nuxt-link>
        </li>

        <li class="main-menu-item">
          <nuxt-link to="/about-us">¿Quiénes somos?</nuxt-link>
        </li>

        <li class="main-menu-item">
          <nuxt-link to="/projects">Proyectos</nuxt-link>
        </li>

        <li class="main-menu-item">
          <nuxt-link to="/contact-us">Contactanos</nuxt-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "MainMenu",
  data: () => {
    return {
      openMenu: false,
    };
  },
  methods: {
    toggleMenu() {
      this.openMenu = !this.openMenu;
    },
  },
  watch: {
    $route() {
      if (this.openMenu) {
        this.openMenu = false;
      }
    },
  },
};
</script>
