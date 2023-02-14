<template>
  <div class="the_footer w-full">
    <GlobalPadding>
      <div class="flex pt-16 pb-3">
        <div
          class="logo_language w-1/4 flex flex-col items-start justify-between"
        >
          <a class="hover:opacity-80 duration-300 ease-in-out" href="">
            <img
              class="h-10"
              src="../assets/images/bunq_logo_white.svg"
              alt=""
            />
          </a>
          <a
            href=""
            class="py-3 px-5 mt-5 bg-white text-black font-semibold rounded-full hover:opacity-75 duration-300"
            >English</a
          >
        </div>
        <div class="links_container flex w-2/4 gap-28">
          <div class="left flex flex-col gap-4">
            <h1 class="text-white font-semibold mb-2">Company</h1>
            <a href="">Mortgages</a>
            <a href="">About us</a>
            <a href="">Jobs</a>
            <a href="">Blog</a>
            <a href="">Press</a>
          </div>
          <div class="right flex flex-col gap-4">
            <h1 class="text-white font-semibold mb-2">Help</h1>
            <a href="">Help Center</a>
            <a href="">Contact</a>
            <a href="">Terms & Policies</a>
            <a class="text-gray-400 hover:text-gray-500" href="">Developer</a>
          </div>
        </div>
        <div
          class="platform_links w-1/4 flex flex-col items-end justify-between"
        >
          <div class="flex gap-4">
            <a href="">
              <img src="../assets/images/instagram_icon.svg" alt="" />
            </a>
            <a href="">
              <img src="../assets/images/twitter_icon.svg" alt="" />
            </a>
            <a href="">
              <img src="../assets/images/linkedin_icon.svg" alt="" />
            </a>
            <a href="">
              <img src="../assets/images/facebook_icon.svg" alt="" />
            </a>
          </div>
          <div class="flex justify-end gap-4">
            <a href="">
              <img class="h-10" src="../assets/images/appstore.svg" alt="" />
            </a>
            <a href="">
              <img
                class="h-10"
                src="../assets/images/googleplay_large_icon.svg"
                alt=""
              />
            </a>
          </div>
        </div>
      </div>
      <div class="gray_line w-full mt-5"></div>
      <div class="foot_links flex text-xs py-5 gap-5">
        <p>© 2023 bunq</p>
        <a class="underline" href="">Privacy</a>
        <a class="underline" href="">Pricing</a>
        <a class="underline" href="">Site Map</a>
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
