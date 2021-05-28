<template>
  <header class="main-header">
    <div class="container">
      <nuxt-link to="/">
        <img
          class="main-header-logo"
          src="~/assets/images/svg/logo.svg"
          alt="Logo EDsoft"
        />
      </nuxt-link>

      <input
        type="checkbox"
        id="btn-toggle-theme"
        class="toggle-switch toggle-color-mode"
        :checked="checked"
        @click="changeTheme()"
      />

      <MainMenu />
    </div>
  </header>
</template>

<script>
import MainMenu from "~/components/MainMenu";

export default {
  name: "MainHeader",
  components: {
    MainMenu,
  },
  data: () => {
    return {
      prueba: false,
    };
  },
  methods: {
    changeTheme() {
      this.$colorMode.preference = this.toggleMode;
    },
  },
  computed: {
    toggleMode() {
      return this.$colorMode.preference === "light" ? "dark" : "light";
    },
    checked() {
      return this.$colorMode.preference === "light" ? false : true;
    },
  },
};
</script>
