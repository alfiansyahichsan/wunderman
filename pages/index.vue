<template>
  <div>
    <Hero />
    <button @click="switchComponent">test</button>
    <section class="mx-auto container py-8">
      <transition name="fade" mode="out-in">
        <div :is="currentComp"></div>
      </transition>
    </section>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from '@vue/composition-api'
import Hero from '../components/Hero.vue'
import AboutWho from '../components/About/Who.vue'
import AboutWhat from '../components/About/What.vue'
// import About from '../components/About.vue'

export default defineComponent({
  name: 'HomePage',
  components: {
    Hero,
    AboutWho,
    AboutWhat,
  },

  setup() {
    const currentComp = ref(AboutWho)

    function switchComponent() {
      currentComp.value = AboutWhat
    }

    return {
      currentComp,
      switchComponent,
    }
  },
})
</script>

<style lang="postcss" scoped></style>
