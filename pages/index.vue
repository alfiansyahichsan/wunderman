<template>
  <div>
    <Hero />

    <About />

    <CoreValues />

    <Specialities />
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'
import Hero from '../components/Hero.vue'

export default defineComponent({
  name: 'HomePage',
  components: {
    Hero,
    About: () => import('../components/About.vue'),
    CoreValues: () => import(`../components/CoreValues.vue`),
    Specialities: () => import(`../components/Specialities.vue`),
  },
})
</script>
