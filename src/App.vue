<template>
  <nav>
    <TheNavbar />
  </nav>
  <main>
    <TheHeader />
    <PressLogos />
    <OurPlans />
  </main>
  <footer class="h-screen"></footer>
</template>

<script>
import TheNavbar from "./components/TheNavbar.vue";
import TheHeader from "./components/TheHeader.vue";
import PressLogos from "./components/PressLogos.vue";
import OurPlans from "./components/OurPlans.vue";

export default {
  name: "App",
  components: { TheNavbar, TheHeader, PressLogos, OurPlans },
};
</script>
