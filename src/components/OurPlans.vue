<template>
  <div class="our_plans py-14">
    <GlobalPadding>
      <div class="text-center flex flex-col items-center">
        <h1 class="text-5xl font-extrabold">Our plans</h1>
        <div class="checkbox_container my-20 relative">
          <input
            class="check_box absolute"
            type="checkbox"
            name="check"
            value="checked"
          />
          <button @click="checkFalse" class="absolute top-3 left-5">
            Personal
          </button>
          <button @click="checkTrue" class="absolute top-3 right-5">
            Business
          </button>
        </div>
      </div>
    </GlobalPadding>
  </div>
</template>

<script>
import GlobalPadding from "../layouts/GlobalPadding.vue";

export default {
  data() {
    return {};
  },
  components: { GlobalPadding },
  methods: {
    checkFalse() {
      const checkBox = document.querySelector(".check_box");
      checkBox.checked = false;
      if (checkBox.checked) {
        console.log("true");
      } else {
        console.log("false");
      }
    },
    checkTrue() {
      const checkBox = document.querySelector(".check_box");
      checkBox.checked = true;
      if (checkBox.checked) {
        console.log("true");
      } else {
        console.log("false");
      }
    },
  },
};
</script>
