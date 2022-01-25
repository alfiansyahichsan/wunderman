<template>
  <transition name="slide-fade" mode="out-in">
    <div
      :key="currentIndex"
      class="flex flex-col items-center px-8 sm:px-20 lg:px-24 py-16 mx-auto md:flex-row bg-gray-50 relative w-full"
    >
      <div class="hidden sm:block w-full lg:w-1/3 lg:max-w-lg md:w-1/2">
        <img
          class="object-cover object-center rounded-lg"
          alt="hero"
          src="https://images.unsplash.com/photo-1634926878768-2a5b3c42f139?fit=clamp&w=400&h=400&q=80"
        />
      </div>
      <div
        class="flex flex-col items-start text-left lg:flex-grow md:w-1/2 lg:pl-24 md:pl-16 md:mb-0"
      >
        <h2
          class="mb-2 text-xs font-semibold tracking-widest text-[#777777] uppercase title-font"
        >
          {{ abouts[currentIndex].sub_title }}
        </h2>
        <h1
          class="mb-2 sm:mb-4 sm:text-3xl lg:text-5xl font-black tracking-tighter text-[#029FE4] title-font drop-shadow-lg"
        >
          {{ abouts[currentIndex].title }}
        </h1>
        <p class="mb-8 text-base leading-relaxed text-left text-[#777777]">
          {{ abouts[currentIndex].body }}
        </p>

        <div class="pagination">
          <div>
            <span>{{ `0${currentIndex + 1}` }}</span>
            <span>/</span>
            <span>{{ `0${abouts.length}` }}</span>
          </div>
          <div class="items-center">
            <button
              class="border py-2 px-3 rounded-xs text-xs"
              @click="switchComponent('prev')"
            >
              &larr;
            </button>
            <button
              class="border py-2 px-3 rounded-xs text-xs bg-[#1BA0E1] text-white"
              @click="switchComponent('next')"
            >
              &rarr;
            </button>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'

export default defineComponent({
  name: 'AboutSection',

  setup() {
    const abouts = ref([
      {
        sub_title: 'TECHNOLOGY COMPANY',
        title: 'Who we are',
        body: 'Sed ut perspiciatis unde omnis iste natus sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.',
      },
      {
        sub_title: 'PROFESSIONAL BRAND MANAGEMENT',
        title: 'What we do',
        body: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.',
      },
      {
        sub_title: 'Strategize, Design, Collaborate',
        title: 'How we do',
        body: 'Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse sequam nihil molestiae consequatur.',
      },
    ])

    const currentIndex = ref(0)

    const switchComponent = (direction: string) => {
      switch (direction) {
        case 'prev':
          if (currentIndex.value) currentIndex.value--
          break

        default:
          if (currentIndex.value < 2) currentIndex.value++
          break
      }
    }

    return {
      abouts,
      switchComponent,
      currentIndex,
    }
  },
})
</script>

<style lang="postcss" scoped>
.pagination {
  @apply flex flex-row w-full items-center justify-between;
  div:first-child {
    @apply text-[#777777] flex items-end space-x-2;
    span:first-child {
      @apply font-bold text-2xl;
    }
    span:second-child {
      @apply text-2xl font-light;
    }
  }
}
</style>
