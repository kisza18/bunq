<template>
  <div class="header">
    <GlobalPadding>
      <div class="pt-20 text-white h-full">
        <div
          class="header_container flex items-center justify-between w-full h-full px-7"
        >
          <div class="content w-1/2">
            <h1 class="text-7xl font-extrabold mb-5">bank of</h1>
            <h1 class="text-7xl font-extrabold mb-5">The Free</h1>
            <h3 class="text-2xl font-semibold mb-5">
              Mobile banking that Makes Life Easy.
            </h3>
            <p class="text-lg mb-10">Try now, no strings attached.</p>
            <a
              class="header_btn px-4 py-3 font-semibold rounded-full hover:opacity-75 duration-300 ease-in-out"
              href=""
              >Get started</a
            >
          </div>
          <div class="image w-1/2">
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

<script>
import GlobalPadding from "../layouts/GlobalPadding.vue";

export default {
  components: { GlobalPadding },
};
</script>
