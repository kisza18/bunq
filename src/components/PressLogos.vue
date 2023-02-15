<template>
  <div class="press_logos w-full py-20 mt-20 md:mt-0">
    <GlobalPadding>
      <div
        class="grid logo_container grid-cols-3 lg:grid-cols-6 gap-10 items-center justify-between w-full px-7"
      >
        <a
          class="press_logo opacity-50 hover:opacity-40 duration-300 ease-in-out flex justify-center"
          href=""
          ><img src="../assets/images/forbes_logo.svg" alt=""
        /></a>
        <a
          class="press_logo opacity-50 hover:opacity-40 duration-300 ease-in-out flex justify-center"
          href=""
          ><img src="../assets/images/thefintech.svg" alt=""
        /></a>
        <a
          class="press_logo opacity-50 hover:opacity-40 duration-300 ease-in-out flex justify-center"
          href=""
          ><img src="../assets/images/wired_logo.svg" alt=""
        /></a>
        <a
          class="press_logo opacity-50 hover:opacity-40 duration-300 ease-in-out flex justify-center"
          href=""
          ><img src="../assets/images/techcrunch.svg" alt=""
        /></a>
        <a
          class="press_logo opacity-50 hover:opacity-40 duration-300 ease-in-out flex justify-center"
          href=""
          ><img src="../assets/images/business_insider_logo.svg" alt=""
        /></a>
        <a
          class="press_logo opacity-50 hover:opacity-40 duration-300 ease-in-out flex justify-center"
          href=""
          ><img src="../assets/images/reuters_logo.svg" alt=""
        /></a>
      </div>
    </GlobalPadding>
  </div>
</template>

<script setup>
import GlobalPadding from "../layouts/GlobalPadding.vue";
import gsap from "gsap";
import { onMounted } from "vue";
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
  gsap.fromTo(
    ".logo_container",
    {
      opacity: 0,
      y: 100,
    },
    {
      scrollTrigger: {
        trigger: ".press_logos",
        once: true,
        start: "top-=200px center",
      },
      duration: 1.0,
      opacity: 1,
      y: 0,
    }
  );
});
</script>
