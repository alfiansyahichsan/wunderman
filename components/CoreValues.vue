<template>
  <div class="min-w-screen flex items-center justify-center py-5 relative">
    <div class="w-full bg-white px-5 py-16 text-gray-800 relative">
      <div class="w-full max-w-6xl mx-auto">
        <div class="text-center max-w-xl mx-auto">
          <h1
            class="text-4xl sm:text-5xl lg:text-7xl font-bold mb-5 text-[#029FE4] drop-shadow-lg"
          >
            Our Core Values
          </h1>
          <h3 class="text-sm lg:text-xl mb-5 font-light">
            Ridiculus laoreet libero pretium et, sit vel elementum convallis
            fames. Sit suspendisse etiam eget egestas. Aliquet odio et lectus
            etiam sit. In mauris rutrum ac ut volutpat, ornare nibh diam.
            Montes, vitae, nec amet enim.
          </h3>
        </div>
        <div class="-mx-3 md:flex items-start pt-12">
          <div
            v-for="(item, index) in ourValues"
            :key="index"
            class="px-3 md:w-1/3 transform transition duration-500 hover:scale-110"
          >
            <div
              class="w-full mx-auto sm:rounded-lg sm:border sm:border-gray-200 sm:p-5 text-gray-800 font-light mb-6"
            >
              <div class="w-full flex mb-4 items-center">
                <div
                  class="overflow-hidden w-1 h-6 bg-gray-800 border border-gray-800 rotate-90 ml-4"
                ></div>
                <div class="flex-grow pl-6">
                  <h6 class="font-bold text-sm uppercase text-gray-600">
                    {{ item.title }}
                  </h6>
                </div>
              </div>
              <div class="w-full">
                <p class="text-sm leading-tight">
                  {{ item.body }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <img src="/img/core-values.png" class="ml-auto" alt="" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'

export default defineComponent({
  name: 'CoreValues',

  setup() {
    const ourValues = ref([
      {
        title: 'DEDICATION',
        body: 'Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat.',
      },
      {
        title: 'INTELLECTUAL HONESTY',
        body: 'Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias conse.',
      },
      {
        title: 'CURIOSITY',
        body: 'At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque.',
      },
    ])

    return {
      ourValues,
    }
  },
})
</script>
