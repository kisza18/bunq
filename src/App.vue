<template>
  <nav>
    <TheNavbar />
  </nav>
  <main>
    <TheHeader />
    <PressLogos />
    <OurPlans />
    <TheSection />
  </main>
  <footer class="h-screen"></footer>
</template>

<script>
import TheNavbar from "./components/TheNavbar.vue";
import TheHeader from "./components/TheHeader.vue";
import PressLogos from "./components/PressLogos.vue";
import OurPlans from "./components/OurPlans.vue";
import TheSection from "./components/TheSection.vue";

export default {
  name: "App",
  components: { TheNavbar, TheHeader, PressLogos, OurPlans, TheSection },
};
</script>
