<template>
  <div class="mx-auto overflow-scroll bg-[#509FDD] px-4 py-6">
    <div class="bg-white border h-full p-5 sm:hidden">
      <h1 class="font-bold text-2xl text-[#029FE4]">OUR SPECIALITY</h1>
      <p class="text-[#303030] pt-4 font-light">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod
        libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc
        sit amet congue aliquam.
      </p>

      <div class="snap-x flex snap-mandatory w-full overflow-scroll pt-12">
        <div
          v-for="(item, index) in specialities"
          :key="index"
          class="snap-center flex-shrink-0 flex items-center justify-center w-full flex-col space-y-3"
        >
          <img :src="item.src" class="pb-6" />
          <p class="text-center text-[#A7A7A7] font-light">{{ item.body }}</p>
        </div>
      </div>
    </div>

    <!-- DESKTOP -->
    <div class="text-center my-12 hidden sm:block">
      <div class="text-center max-w-xl mx-auto text-white">
        <h1 class="text-5xl lg:text-7xl font-bold mb-5 drop-shadow-lg">
          OUR SPECIALITY
        </h1>
        <h3 class="text-sm sm:text-xl mb-5 font-light">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod
          libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc
          sit amet congue aliquam.
        </h3>
      </div>
      <div class="grid grid-cols-3 gap-4 sm:w-full lg:w-10/12 mx-auto my-12">
        <div
          v-for="(item, index) in specialities"
          :key="index"
          class="border rounded-lg bg-white shadow-lg sm:p-4 lg:p-8 mx-auto"
        >
          <img :src="item.src" class="pb-6 mx-auto" />
          <p class="font-bold text-sm uppercase text-gray-600">
            {{ item.title }}
          </p>
          <p class="text-center text-[#A7A7A7] font-light pt-4">
            {{ item.body }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'

export default defineComponent({
  name: 'SpecialitiesSection',

  setup() {
    const specialities = ref([
      {
        title: 'Speed Improvement',
        src: '/icons/speed.svg',
        body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc sit amet congue aliquam.',
      },
      {
        title: 'Exhaust',
        src: '/icons/exhaust.svg',
        body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc sit amet congue aliquam.',
      },
      {
        title: 'Accesories',
        src: '/icons/accesories.svg',
        body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc sit amet congue aliquam.',
      },
    ])

    return {
      specialities,
    }
  },
})
</script>
