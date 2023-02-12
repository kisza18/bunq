<template>
  <div class="section">
    <GlobalPadding>
      <div class="pt-20 text-white h-full">
        <div
          class="section_container flex items-center justify-between w-full h-full px-7"
        >
          <div class="content w-1/2">
            <div class="flex items-center mb-6">
              <div class="mr-2">
                <h1 class="text-4xl font-extrabold">We are</h1>
                <div class="h-4 -mt-3"></div>
              </div>
              <div>
                <h1 class="text-4xl font-extrabold">bank of The Free</h1>
                <div class="w-full bg-green-600 h-4 -mt-3"></div>
              </div>
            </div>
            <p class="text-md leading-7 mb-10 font-light tracking-wide">
              The future calls for banks that are sustainable in as many ways as
              possible. We are the only bank in the world that lets you choose
              how your money is invested. We are committed to a green, inclusive
              and diverse future for anyone on the planet.
            </p>
            <a
              class="section_btn px-4 py-3 font-semibold rounded-full hover:opacity-75 bg-white text-black duration-300 ease-in-out"
              href=""
              >Learn more about us</a
            >
          </div>
          <div class="image w-1/2">
            <img
              class="scale-90 pt-10 hover:scale-95 duration-700"
              src="../assets/images/illustration_globe.webp"
              alt="section_image"
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
