<template>
  <div class="header">
    <GlobalPadding>
      <div class="pt-20 text-white h-full">
        <div
          class="header_container flex flex-col md:flex-row items-center justify-between w-full h-full px-7"
        >
          <div class="content md:w-1/2 text-center md:text-left mt-10">
            <h1 class="header_text text-5xl md:text-7xl font-extrabold mb-5">
              bank of
            </h1>
            <h1 class="header_text text-5xl md:text-7xl font-extrabold mb-5">
              The Free
            </h1>
            <h3 class="header_text text-xl md:text-2xl font-semibold mb-5">
              Mobile banking that Makes Life Easy.
            </h3>
            <p class="header_text text-lg mb-10">
              Try now, no strings attached.
            </p>
            <a
              class="header_btn px-20 md:px-4 py-3 font-semibold rounded-full hover:opacity-75 duration-300 ease-in-out"
              href=""
              >Get started</a
            >
          </div>
          <div class="image md:w-1/2">
            <img
              class="scale-90 pt-10"
              src="../assets/images/phone_card.webp"
              alt="header_image"
            />
          </div>
        </div>
      </div>
    </GlobalPadding>
  </div>
</template>

<script setup>
import GlobalPadding from "../layouts/GlobalPadding.vue";
import gsap from "gsap";
import { onMounted } from "vue";

onMounted(() => {
  gsap.fromTo(
    ".header_text",
    {
      opacity: 0,
      y: -100,
    },
    {
      duration: 1.5,
      opacity: 1,
      y: 0,
      ease: "power3.inOut",
    }
  );
});
onMounted(() => {
  gsap.fromTo(
    ".header_btn",
    {
      opacity: 0,
    },
    {
      duration: 0.5,
      opacity: 1,
      ease: "power1.inOut",
      delay: 0.5,
    }
  );
});
</script>
