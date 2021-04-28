<template>
  <q-page class="flex flex-center">
    <img
      ref="logo"
      alt="Quasar logo"
      src="~assets/logo_teal.svg"
    >
  </q-page>
</template>

<script>
import gsap from 'gsap';
export default {
  mounted() {
    gsap.from(this.$refs.logo, { opacity: 0, x: -40, scale: 0.7, duration: 3, ease: 'power3.out' });
  }
}
</script>

<style scoped>
.logo {
  opacity: 1;
  transform: scale(1), translateX(0);
}
</style>
