<template>
  <nav>
    <TheNavbar />
  </nav>
  <main class="h-screen"></main>
  <footer class="h-screen"></footer>
</template>

<script>
import TheNavbar from "./components/TheNavbar.vue";

export default {
  name: "App",
  components: { TheNavbar },
};
</script>
