<template>
  <div class="container-fluid">
    <MainHeader />
    <main>
      <Nuxt />
    </main>
    <MainFooter />
  </div>
</template>

<script>
import MainHeader from "~/components/MainHeader";
import MainFooter from "~/components/MainFooter";

export default {
  name: "DefaultLayout",
  components: {
    MainHeader,
    MainFooter,
  },
};
</script>
