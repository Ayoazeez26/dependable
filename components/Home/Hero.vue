<script setup lang="ts"></script>
<template>
  <div class="py-20 px-4 xl:px-0 md:py-28 w-full">
    <!-- <img class="hidden lg:block" src="https://s3.eu-west-2.amazonaws.com/dependable.com/hero-img.png" alt="video image" />
    <img class="lg:hidden" src="https://s3.eu-west-2.amazonaws.com/dependable.com/hero-img-mob.png" alt="video image" /> -->
    <div class="w-full max-w-[1240px] flex mx-auto lg:mt-[120px]">
      <div
        class="flex flex-col justify-between lg:flex-row lg:items-center gap-10 w-full max-w-[1240px]"
      >
        <div class="flex flex-col w-full mt-10 md:mt-0 lg:max-w-[572px]">
          <h2
            class="font-semibold text-secondary text-[26px] md:text-[32px] lg:text-[56px] lg:leading-[72px] leading-[42px] md:leading-[48px]"
          >
            <span class="text-primary">A</span> Dependable Healthcare Service
          </h2>
          <p class="mt-2 md:mt-6 leading-7 md:text-lg">
            We're not just a care team; we're your happiness accomplices! Our
            mission is simple - to serve you with unparalleled excellence and
            genuine compassion.
          </p>
          <div
            class="flex flex-col w-full mt-10 md:w-auto md:flex-row md:items-center"
          >
            <nuxt-link
              to="/contact"
              class="bg-secondary border-2 border-secondary text-center font-medium py-3 px-10 rounded-lg text-white"
            >
              Get in Touch
            </nuxt-link>
          </div>
        </div>
        <img
          class="w-full hidden lg:block max-w-[612px]"
          src="https://s3.eu-west-2.amazonaws.com/dependable.com/hero-img.png"
        />
        <img
          class="w-full lg:hidden"
          src="https://s3.eu-west-2.amazonaws.com/dependable.com/hero-mob-img.png"
        />
      </div>
    </div>
    <!-- <div class="w-full max-w-[1240px] flex mx-auto mt-10 lg:mt-[68px]">
      <div
        class="flex flex-col justify-between lg:flex-row w-full max-w-[1240px]"
      >
        <h1
          class="font-semibold text-head leading-snug text-[38px] lg:leading-snug lg:text-[48px] w-full max-w-[572px]"
        >
          Connecting Healthcare Professionals with their Dream Jobs
        </h1>
        <div class="flex flex-col w-full max-w-[612px]">
          <p class="mt-4 lg:mt-0 leading-[28px] md:leading-[28px] md:text-lg">
            At Wana Services, we specialize in sourcing local job opportunities
            for Nurses, Care Assistants, Support Workers, and Social Workers.
            Our mission is to help healthcare professionals find fulfilling
            careers in their own communities.
          </p>
          <div
            class="flex flex-col lg:flex-row items-stretch lg:items-center gap-4 mt-10"
          >
            <button
              class="bg-secondary border-2 border-secondary font-semibold px-4 py-3 md:w-[160px] rounded-lg text-white"
            >
              Join
            </button>
            <button
              class="bg-white border-2 border-secondary font-semibold px-4 py-3 md:w-[160px] rounded-lg text-secondary"
            >
              Learn More
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="w-full max-w-[1240px] flex mx-auto mt-20 md:mt-[120px]">
      <div
        class="flex flex-col justify-between lg:flex-row lg:items-center w-full max-w-[1240px]"
      >
        <div
          class="slide-parent border-l-4 flex flex-col w-full max-w-[572px] mb-10 md:mb-0"
        >
          <div class="slide-child w-full pl-6 py-4 -translate-x-1">
            <h2
              class="font-semibold text-lg md:text-xl leading-[34px] md:leading-[48px]"
            >
              Experienced and Qualified Staff
            </h2>
            <p class="mt-2 mb-3">
              Our dedicated team understands the importance of finding work in
              your city or town, and we are here to help you every step of the
              way.
            </p>
            <nuxt-link
              to="/jobCandidate"
              class="text-secondary font-bold py-2 text-sm"
              >Register as a Candidate
              <Icon name="mdi:arrow-right" size="20"></Icon
            ></nuxt-link>
          </div>
          <div class="w-full pl-6 py-4 -translate-x-1">
            <h2 class="font-semibold text-xl leading-[48px]">
              Talented Healthcare Professionals
            </h2>
            <p class="mt-2 mb-3">
              Schedule appointments with qualified healthcare providers to
              address your health concerns.
            </p>
            <nuxt-link
              to="/jobClient"
              class="text-secondary font-bold py-2 text-sm"
              >Book Staff <Icon name="mdi:arrow-right" size="20"></Icon
            ></nuxt-link>
          </div>
          <div class="w-full pl-6 py-4 -translate-x-1">
            <h2 class="font-semibold text-xl leading-[48px]">
              Flexible Job Opportunities
            </h2>
            <p class="mt-2 mb-3">
              If you’re a qualified nurse, midwife, or care assistant looking
              for bank work, Wana Services can help you find flexible shifts
              with 24/7 support.
            </p>
            <nuxt-link
              to="/applyNow"
              class="text-secondary font-bold py-2 text-sm"
              >Apply Now <Icon name="mdi:arrow-right" size="20"></Icon
            ></nuxt-link>
          </div>
        </div>
        <img class="w-full max-w-[612px]" src="https://s3.eu-west-2.amazonaws.com/dependable.com/staff.png" />
      </div>
    </div> -->
  </div>
</template>

<style lang="scss" scoped>
.slide-child {
  border-left: 4px solid #cb9821;
}
</style>
