<template>
  <div class="w-full">
    <Header />
    <transition name="fade" mode="out-in">
      <Nuxt />
    </transition>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'
import Header from '../components/Header.vue'

export default defineComponent({
  name: 'DefaultLayout',
  components: {
    Header,
  },
})
</script>

<style lang="postcss">
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
