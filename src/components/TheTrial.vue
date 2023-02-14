<template>
  <div class="the_trial">
    <GlobalPadding>
      <div class="flex flex-col items-center justify-center text-white py-16">
        <h1 class="text-4xl font-extrabold mb-10">
          Start your 30-day free trial
        </h1>
        <p class="mb-8">
          Open your account in just 5 minutes, directly from your smartphone.
        </p>
        <a
          class="header_btn z-10 px-4 py-3 font-semibold rounded-full hover:opacity-75 duration-300 ease-in-out"
          href=""
          >Get started</a
        >
        <img
          class="scale-75 -mt-20 z-0"
          src="../assets/images/rainbow_phone.png"
          alt=""
        />
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
