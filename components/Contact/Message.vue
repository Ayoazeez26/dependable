<script setup lang="ts">
const active = ref("all");
const roles = ref([
  {
    title: "Product Designer",
    category: "Design",
    type: "Remote",
    to: "/job",
    duration: "Contract",
  },
  {
    title: "Engineering Manager",
    category: "Software Development",
    type: "Semi-Remote",
    to: "/job",
    duration: "Part-time",
  },
  {
    title: "Customer Success Manager",
    category: "Customer Success",
    type: "On-site",
    to: "/job",
    duration: "Full-time",
  },
  {
    title: "Account Executive",
    category: "Sales",
    type: "Remote",
    to: "/job",
    duration: "Part-time",
  },
  {
    title: "SEO Marketing Manager",
    category: "Marketing",
    type: "Semi-Remote",
    to: "/job",
    duration: "Full-time",
  },
]);

const submitForm = () => {
  console.log("submitting form");
};

const errorMsg = reactive({});
const firstname = ref("");
const lastname = ref("");
const company = ref("");
const email = ref("");
const message = ref("");
const subject = ref("");
const phone = ref("");

const validateEmail = (email) => {
  if (/^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(email)) {
    errorMsg.email = "";
  } else {
    errorMsg.email = "Invalid Email Address";
  }
};

const validateInput = (input, value) => {
  if (value) {
    errorMsg[input] = "";
  } else {
    errorMsg[input] = "Required";
  }
};

watch(name, (value) => {
  validateInput("name", value);
});

watch(email, (value) => {
  validateEmail(value);
});

watch(message, (value) => {
  validateInput("message", value);
});
</script>
<template>
  <div
    class="w-full max-w-[1240px] mx-auto py-16 md:py-12 overflow-x-hidden relative"
  >
    <div class="w-full flex flex-col items-center lg:gap-[56px]">
      <img
        src="https://s3.eu-west-2.amazonaws.com/dependable.com/contact-img.png"
        alt="touch"
      />
      <div
        class="py-20 gap-6 flex justify-center border-b border-grey-4 flex-wrap"
      >
        <div
          class="flex flex-col items-start gap-10 p-6 rounded-lg border border-grey-4 bg-grey-2 h-[280px] w-[327px]"
        >
          <div class="bg-blue-2 p-2 rounded">
            <img src="/svg/chat.svg" alt="chat" />
          </div>
          <div class="flex flex-col">
            <h6 class="font-medium leading-8">Email</h6>
            <p class="text-grey-5 mt-2 text-sm">Send them a private message</p>
            <a
              class="underline mt-3 text-sm"
              href="mailto:info@dependablehealth.co.uk"
              >info@dependablehealth.co.uk</a
            >
          </div>
        </div>
        <div
          class="flex flex-col items-start gap-10 p-6 rounded-lg border border-grey-4 bg-grey-2 h-[280px] w-[327px]"
        >
          <div class="bg-blue-2 p-2 rounded">
            <img src="/svg/phone.svg" alt="phone" />
          </div>
          <div class="flex flex-col">
            <h6 class="font-medium leading-8">Telephone</h6>
            <p class="text-grey-5 mt-2 text-sm">Schedule a call with them</p>
            <p class="underline mt-3 text-sm">+44 1484 506700</p>
          </div>
        </div>
        <div
          class="flex flex-col items-start gap-10 p-6 rounded-lg border border-grey-4 bg-grey-2 h-[280px] w-[327px]"
        >
          <div class="bg-blue-2 p-2 rounded">
            <img src="/svg/location.svg" alt="location" />
          </div>
          <div class="flex flex-col">
            <h6 class="font-medium leading-8">Address</h6>
            <p class="text-grey-5 mt-2 text-sm">Visit their office HQ</p>
            <p class="underline mt-3 text-sm">
              100 Smith Street Collingwood VIC 3066 AU
            </p>
          </div>
        </div>
      </div>
      <div
        class="flex flex-col items-center px-4 xl:px-0 py-20 gap-x-2 md:px-16 max-w-[619px] w-full"
      >
        <h3 class="text-head font-semibold text-[32px] lg:text-[48px]">
          Message Us Directly
        </h3>
        <p class="mt-1 md:text-lg tracking-wide">
          Our friendly team would love to hear from you
        </p>

        <div class="w-full mt-10">
          <form
            id="getLicense"
            class="w-full flex flex-col items-start"
            @submit.prevent="submitForm"
          >
            <div class="w-full flex flex-col md:flex-row md:gap-4">
              <div class="w-full">
                <label for="firstName" class="mb-2">First Name</label>
                <input
                  id="firstName"
                  v-model="firstname"
                  type="text"
                  name="firstName"
                  required
                  class="border border-grey-6 bg-transparent rounded-lg py-4 pl-6 pr-2 focus:outline-none w-full h-12"
                  :class="errorMsg.name ? 'border border-red-500' : ''"
                  placeholder="John"
                />
                <span v-if="errorMsg.name" class="text-red-500 text-xs mt-1">{{
                  errorMsg.name
                }}</span>
                <span v-else class="text-transparent text-xs mt-1"
                  >There is no error message</span
                >
              </div>
              <div class="w-full">
                <label for="lastName" class="mb-2">Last Name</label>
                <input
                  id="lastName"
                  v-model="lastname"
                  type="text"
                  name="lastName"
                  required
                  class="border border-grey-6 bg-transparent rounded-lg py-4 pl-6 pr-2 focus:outline-none w-full h-12"
                  :class="errorMsg.name ? 'border border-red-500' : ''"
                  placeholder="Doe"
                />
                <span v-if="errorMsg.name" class="text-red-500 text-xs mt-1">{{
                  errorMsg.name
                }}</span>
                <span v-else class="text-transparent text-xs mt-1"
                  >There is no error message</span
                >
              </div>
            </div>
            <div class="w-full">
              <div class="flex flex-col w-full">
                <label for="email">Email Address</label>
                <input
                  id="email"
                  v-model="email"
                  type="email"
                  name="email"
                  required
                  class="border border-grey-6 bg-transparent rounded-lg py-4 pl-6 pr-2 focus:outline-none h-12"
                  :class="errorMsg.email ? 'border border-red-500' : ''"
                  placeholder="Enter your email address"
                />
                <span v-if="errorMsg.email" class="text-red-500 text-xs mt-1">{{
                  errorMsg.email
                }}</span>
                <span v-else class="text-transparent text-xs mt-1"
                  >There is no error message</span
                >
              </div>
            </div>
            <div class="flex w-full">
              <div class="flex flex-col w-full">
                <label for="message">Message</label>
                <textarea
                  id="message"
                  v-model="message"
                  name="message"
                  rows="5"
                  cols="30"
                  class="border border-grey-6 bg-transparent rounded-lg py-4 px-6 focus:outline-none"
                  placeholder="Leave us a message"
                  maxlength="500"
                />
                <span
                  v-if="errorMsg.message"
                  class="text-red-500 text-xs mt-1"
                  >{{ errorMsg.message }}</span
                >
                <span v-else class="text-transparent text-xs mt-1"
                  >There is no error message</span
                >
                <!-- <p class="text-grey-4 italic">
                * Please limit your message to 500 characters
              </p> -->
              </div>
            </div>
            <div class="w-full mt-6">
              <button
                type="submit"
                class="liquor-btn min-w-max py-3 px-10 leading-none rounded-lg text-sm sm:text-base bg-secondary text-white w-full hover:bg-secondary/90"
              >
                Send Message
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
li {
  background: url("/svg/list.svg") no-repeat left top + 5px;
  padding: 3px 0 3px 40px;
  list-style: none;
  margin: 0;
  line-height: 28px;
}
</style>
