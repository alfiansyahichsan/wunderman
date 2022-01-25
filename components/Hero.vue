<template>
  <div class="hero">
    <div class="left-side">
      <div class="content">
        <div class="clip-2"></div>
        <div class="clip-1"></div>
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
  @apply flex flex-col-reverse sm:flex-row sm:h-screen sm:-mt-16;

  .left-side {
    @apply flex items-center text-left text-white sm:mt-0 z-20 relative w-full;

    .content {
      @apply w-full px-8 sm:pt-0 py-6 md:px-12 lg:px-24 relative bg-[#4097DB] sm:bg-white z-20;

      .clip-1 {
        @apply absolute sm:hidden bg-[#4097DB] sm:bg-white h-full -mt-16 w-full left-0 -z-10;
        clip-path: polygon(0% 0%, 100% 30%, 100% 100%, 0 100%);
      }

      .clip-2 {
        @apply absolute sm:hidden bg-[#53A7E9] sm:bg-white h-32 -mt-12 w-full left-0 -z-10;
        clip-path: polygon(0% 30%, 100% 0%, 100% 100%, 0% 100%);
      }

      h2 {
        @apply text-3xl font-bold text-white sm:text-gray-800 md:text-5xl drop-shadow-lg;
      }

      span {
        @apply font-extrabold text-white sm:!text-[#029FE4];
      }

      p {
        @apply mt-2 text-sm text-white sm:text-gray-500 md:text-base;
      }
    }
  }

  .right-side {
    @apply w-full lg:block -z-10;
    clip-path: polygon(10% 0, 100% 0%, 100% 100%, 0 100%);
    @media only screen and (max-width: 600px) {
      clip-path: polygon(0% 0, 100% 0%, 100% 100%, 0 100%);
    }

    div {
      @apply h-full object-cover;
      img {
        @apply w-full h-full object-cover;
      }
    }
  }
}
</style>
