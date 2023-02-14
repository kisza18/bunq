<template>
  <div class="our_plans pt-14">
    <GlobalPadding>
      <!-- CheckBox -->
      <div class="text-center flex flex-col items-center">
        <h1 class="text-5xl font-extrabold">Our plans</h1>
        <div class="checkbox_container mt-20 mb-10 relative">
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
      <!-- Change Content -->
      <div class="text-center">
        <!-- Personal -->
        <div
          v-show="!change"
          class="personal_class flex flex-col md:flex-row items-center justify-center"
        >
          <h1 class="flex items-center justify-center px-2">
            <img class="px-2" src="../assets/images/blue_check.svg" alt="" />
            Enjoy a 30-day free trial of any plan
          </h1>
          <h1 class="flex items-center justify-center px-2">
            <img class="px-2" src="../assets/images/blue_check.svg" alt="" />
            Switch or cancel your plan anytime
          </h1>
        </div>

        <!-- Business -->
        <div
          v-show="change"
          class="business_class flex items-center justify-center"
        >
          <h1 class="flex items-center justify-center px-2">
            <img class="px-2" src="../assets/images/blue_check.svg" alt="" />
            Switch or cancel your plan anytime
          </h1>
        </div>

        <!-- Cards -->
        <div class="flex items-center justify-center mt-12">
          <div class="card_container flex gap-5 overflow-x-scroll">
            <div
              class="card flex-shrink-0 flex flex-col items-center justify-center col-span-1 w-72 rounded-3xl py-9 px-6 border-2"
            >
              <img class="w-12" src="../assets/images/green_tree.svg" alt="" />
              <h1 class="pt-6 pb-3 text-2xl font-semibold">Easy Green</h1>
              <p
                v-show="!change"
                class="text-sm font-light pt-2 pb-5 tracking-wide leading-7"
              >
                Open your sustainable bank account to become CO2-free in just 2
                years with zero effort.
              </p>
              <p
                v-show="change"
                class="text-sm font-light pt-2 pb-5 tracking-wide leading-7"
              >
                Effortlessly offset CO2 while you spend and make your business
                sustainable.
              </p>
              <p class="text-sm">
                <span v-show="!change" class="font-bold">€17.99</span
                ><span v-show="change" class="font-bold">€22.99</span>/month
              </p>
              <a
                href=""
                class="py-3 px-8 mt-5 bg-white text-black font-semibold rounded-full hover:opacity-75 duration-300"
                >Discover Easy Green</a
              >
            </div>
            <div
              class="card flex-shrink-0 relative overflow-hidden card_popular flex flex-col items-center justify-center col-span-1 w-72 rounded-3xl py-9 px-5 border-2"
            >
              <div
                class="popular_class absolute top-0 -right-3 flex items-center justify-between rounded-b-2xl py-1 px-2"
              >
                <img class="w-4" src="../assets/images/star_icon.svg" alt="" />
                <h1 class="text-white text-sm mr-4">Most popular</h1>
              </div>
              <img
                class="w-12"
                src="../assets/images/blue_diamond.svg"
                alt=""
              />
              <h1 class="pt-6 pb-3 text-2xl font-semibold">Easy Money</h1>
              <p
                v-show="!change"
                class="text-sm font-light pt-2 pb-5 tracking-wide leading-7"
              >
                Budget, save and bank like a local with multiple EU IBANs in
                over 15 different currencies.
              </p>
              <p
                v-show="change"
                class="text-sm font-light pt-2 pb-5 tracking-wide leading-7"
              >
                Do business like a local all over Europe with multiple EU IBANs
                in over 15 different currencies.
              </p>
              <p class="text-sm">
                <span v-show="!change" class="font-bold">€8.99</span
                ><span v-show="change" class="font-bold">€12.99</span>/month
              </p>
              <a
                href=""
                class="py-3 px-8 mt-5 bg-white text-black font-semibold rounded-full hover:opacity-75 duration-300"
                >Discover Easy Money</a
              >
            </div>
            <div
              class="card flex-shrink-0 flex flex-col items-center justify-center col-span-1 w-72 rounded-3xl py-9 px-6 border-2"
            >
              <img class="w-12" src="../assets/images/yellow_bank.svg" alt="" />
              <h1 class="pt-6 pb-3 text-2xl font-semibold">Easy Bank</h1>
              <p
                v-show="!change"
                class="text-sm font-light pt-2 pb-5 tracking-wide leading-7"
              >
                Get a bank account in just 5 minutes to save time and money on
                instant payments.
              </p>
              <p
                v-show="change"
                class="text-sm font-light pt-2 pb-5 tracking-wide leading-7"
              >
                Open your business account in 5 minutes to instantly save time
                and money.
              </p>
              <p class="text-sm">
                <span v-show="!change" class="font-bold">€2.99</span
                ><span v-show="change" class="font-bold">€6.99</span>/month
              </p>
              <a
                href=""
                class="py-3 px-8 mt-5 bg-white text-black font-semibold rounded-full hover:opacity-75 duration-300"
                >Discover Easy Bank</a
              >
            </div>
            <div
              class="card flex-shrink-0 flex flex-col items-center justify-center col-span-1 w-72 rounded-3xl py-9 px-5 border-2"
            >
              <img
                class="w-12"
                src="../assets/images/light_blue_piggy.svg"
                alt=""
              />
              <h1 class="pt-6 pb-3 text-2xl font-semibold">Easy Savings</h1>
              <p
                v-show="!change"
                class="text-sm font-light pt-2 pb-5 tracking-wide leading-7"
              >
                The savings account with a kick! Sign up in 5 minutes to earn
                high interest with zero fees.
              </p>
              <p
                v-show="change"
                class="text-sm font-light pt-2 pb-5 tracking-wide leading-7"
              >
                Sign up in 5 minutes to earn high interest on your business
                capital with zero fees.
              </p>
              <p v-show="!change" class="text-sm">
                <span class="font-bold">€17.99</span>/month
              </p>
              <p v-show="change" class="text-sm font-bold">Free</p>
              <a
                href=""
                class="py-3 px-7 mt-5 bg-white text-black font-semibold rounded-full hover:opacity-75 duration-300"
                >Discover Easy Savings</a
              >
            </div>
          </div>
        </div>
      </div>
    </GlobalPadding>
  </div>
</template>

<script>
import GlobalPadding from "../layouts/GlobalPadding.vue";

export default {
  data() {
    return {
      change: false,
    };
  },
  components: { GlobalPadding },
  methods: {
    checkFalse() {
      const checkBox = document.querySelector(".check_box");
      checkBox.checked = false;
      if (checkBox.checked) {
        this.change = true;
      } else {
        this.change = false;
      }
    },
    checkTrue() {
      const checkBox = document.querySelector(".check_box");
      checkBox.checked = true;
      if (checkBox.checked) {
        this.change = true;
      } else {
        this.change = false;
      }
    },
  },
};
</script>
