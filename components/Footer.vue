<template>
  <footer class="w-full bg-[#07477A] text-white relative">
    <div
      class="bg-[#08385F] h-48 absolute bottom-0 w-full"
      style="clip-path: polygon(0% 0%, 100% 100%, 100% 100%, 0 100%)"
    ></div>
    <div
      class="bg-[#14619D] h-48 absolute bottom-0 w-full"
      style="clip-path: polygon(0% 100%, 100% 0%, 100% 100%, 0% 100%)"
    ></div>
    <div class="xl:px-40 pb-24 lg:px-20 md:px-10 px-5">
      <div
        class="w-full pt-12 flex flex-col sm:flex-row space-y-2 justify-start text-xs"
      >
        <div class="w-full sm:w-1/3 pr-6 flex flex-col space-y-4 pb-4">
          <img src="/icons/logo-white.svg" alt="company" class="w-48" />
          <p class="opacity-60">
            Jl. Lembong No 8 Kel. Braga Kec. Sumur Bandung, Kota Bandung, Jawa
            Barat
          </p>
        </div>
        <div class="w-full sm:w-1/4 flex flex-col pb-2">
          <a class="opacity-70">Who We Are</a>
        </div>
        <div class="w-full sm:w-1/4 flex flex-col pb-2">
          <a class="opacity-70">Our Values</a>
        </div>
        <div class="w-full sm:w-1/4 flex flex-col pb-2">
          <a class="opacity-70">The Perks</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
export default {
  name: 'FooterNavigation',
}
</script>
