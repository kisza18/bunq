<template>
  <nav>
    <TheNavbar />
  </nav>
  <main>
    <TheHeader />
    <PressLogos />
    <OurPlans />
    <TheSection />
    <TheReview />
    <TheTrial />
  </main>
  <footer>
    <TheFooter />
  </footer>
</template>

<script>
import TheNavbar from "./components/TheNavbar.vue";
import TheHeader from "./components/TheHeader.vue";
import PressLogos from "./components/PressLogos.vue";
import OurPlans from "./components/OurPlans.vue";
import TheSection from "./components/TheSection.vue";
import TheReview from "./components/TheReviews.vue";
import TheTrial from "./components/TheTrial.vue";
import TheFooter from "./components/TheFooter.vue";

export default {
  name: "App",
  components: {
    TheNavbar,
    TheHeader,
    PressLogos,
    OurPlans,
    TheSection,
    TheReview,
    TheTrial,
    TheFooter,
  },
};
</script>
