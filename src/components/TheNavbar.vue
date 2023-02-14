<template>
  <div>
    <div
      class="navbar h-20 w-full border-b z-30"
      :class="{ 'navbar--hidden': !showNavbar }"
    >
      <GlobalPadding>
        <div class="nav_container flex justify-between items-center h-full">
          <div class="left_container flex items-center">
            <a href="" class="logo">
              <img
                class="h-10 opacity-100 hover:opacity-80 duration-300 ease-in-out"
                src="../assets/images/bunq_logo_white.svg"
                alt="logo"
              />
            </a>
            <div class="hiring rounded-2xl text-sm ml-6">
              <a href="" class="animation px-2 py-2 flex items-center">
                <div class="hand mr-2">👋</div>
                <div>We're hiring!</div>
              </a>
            </div>
          </div>
          <div class="right_container">
            <div class="flex items-center justify-center">
              <a
                class="compare duration-300 ease-in-out font-semibold mr-8"
                href=""
                >Compare plans</a
              >
              <a
                class="join px-4 py-2 font-semibold rounded-full duration-300 ease-in-out mr-4"
                href=""
                >Join us now</a
              >
              <a
                class="login px-4 py-2 font-semibold rounded-full hover:opacity-75 duration-300 ease-in-out mr-11"
                href=""
                >Log in</a
              >
              <div class="nav_bar" @click="toggleNav()">
                <div class="bar1"></div>
                <div class="bar2"></div>
                <div class="bar3"></div>
              </div>
            </div>
          </div>
        </div>
      </GlobalPadding>
    </div>
    <div
      class="navbar_menu absolute z-20 h-full w-full bg-black opacity-80 mt-20 hide_nav hidden"
    >
      <div
        class="nav_items_container w-full h-full flex items-center justify-center"
      >
        <div
          class="nav_items flex flex-col text-5xl text-center font-bold -mt-44 items-center"
        >
          <div class="link_container flex flex-col mb-10">
            <a class="z-10 px-2" href="">Business</a>
            <div class="link_underline deep_blue z-0 w-full h-4 -mt-3"></div>
          </div>
          <div class="link_container flex flex-col mb-10">
            <a class="z-10 px-2" href="">About us</a>
            <div class="link_underline fuchsia z-0 w-full h-4 -mt-3"></div>
          </div>
          <div class="link_container flex flex-col mb-10">
            <a class="z-10 px-2" href="">Help Center</a>
            <div class="link_underline turquoise z-0 w-full h-4 -mt-3"></div>
          </div>
          <div class="link_container flex flex-col mb-10">
            <a class="z-10 px-2" href="">Jobs</a>
            <div class="link_underline deep_purple z-0 w-full h-4 -mt-3"></div>
          </div>
          <div class="link_container flex flex-col">
            <a class="z-10 px-2" href="">Press</a>
            <div class="link_underline orange z-0 w-full h-4 -mt-3"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import GlobalPadding from "../layouts/GlobalPadding.vue";

export default {
  data() {
    return {
      showNavbar: true,
      lastScrollPosition: 0,
      toggleMenu: false,
    };
  },
  name: "TheNavbar",
  components: { GlobalPadding },
  methods: {
    toggleNav() {
      const navBar = document.querySelector(".nav_bar");
      const navBarMenu = document.querySelector(".navbar_menu");
      const body = document.body;
      navBarMenu.classList.remove("hidden");
      navBar.classList.toggle("change");
      navBarMenu.classList.toggle("hide_nav");
      this.toggleMenu = !this.toggleMenu;

      body.style.overflow === ""
        ? (body.style.overflow = "hidden")
        : (body.style.overflow = "");
    },
    onScroll() {
      const currentScrollPosition =
        window.pageYOffset || document.documentElement.scrollTop;
      if (Math.abs(currentScrollPosition - this.lastScrollPosition) < 60) {
        return;
      }

      this.showNavbar = currentScrollPosition < this.lastScrollPosition;
      this.lastScrollPosition = currentScrollPosition;
    },
  },
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
  },
};
</script>
