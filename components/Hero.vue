<template>
  <div class="hero">
    <div class="left-side">
      <div class="clip-1"></div>
      <div class="clip-2"></div>
      <div class="content">
        <h2>
          Discover Your
          <span>Wonder</span>
        </h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam.
        </p>
      </div>
    </div>
    <div class="right-side">
      <div>
        <!-- <div class="h-full bg-black opacity-25"></div> -->
        <img src="/img/banner.png" alt="banner" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'HeroBanner',
}
</script>

<style lang="postcss" scoped>
.hero {
  @apply flex flex-col-reverse sm:flex-row h-full bg-[#53A7E9] sm:bg-white;

  .left-side {
    @apply flex items-center text-left text-white mt-8 sm:mt-0 z-20 relative w-full;

    .clip-1 {
      @apply absolute sm:hidden bg-[#4097DB] sm:bg-white h-72 w-full z-20;
      clip-path: polygon(0% 0%, 100% 20%, 100% 100%, 0 100%);
    }

    .clip-2 {
      @apply absolute sm:hidden bg-[#53A7E9] sm:bg-white w-full h-72 z-10;
      clip-path: polygon(0% 30%, 100% 0%, 100% 100%, 0% 100%);
    }

    .content {
      @apply w-full px-8 sm:pt-0 sm:py-0 md:px-12 lg:px-24 z-40;

      h2 {
        @apply text-3xl font-bold text-white sm:text-gray-800 md:text-5xl drop-shadow-lg;
      }

      span {
        @apply font-extrabold text-white sm:!text-[#4097DA];
      }

      p {
        @apply mt-2 text-sm text-white sm:text-gray-500 md:text-base;
      }
    }
  }

  .right-side {
    @apply w-full lg:block;
    clip-path: polygon(10% 0, 100% 0%, 100% 100%, 0 100%);
    @media only screen and (max-width: 600px) {
      clip-path: polygon(0% 0, 100% 0%, 100% 100%, 0 100%);
    }

    div {
      @apply h-full object-cover;
      img {
        @apply w-full h-full;
      }
    }
  }
}
</style>
