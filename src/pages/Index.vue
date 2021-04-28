<template>
  <q-page class="flex flex-center front-page">
    <img id="bg" src="~/assets/bg.jpg" />
    <div class="fog-container">
    <img src="~/assets/fog.png" />
    <img src="~/assets/fog.png" />
    </div>
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
.front-page {
  overflow: hidden;
}
#bg {
  position: absolute;
  height: 100%;
  width: 100%;
  filter: opacity(0.1);
}
.fog-container {
  position:absolute;
  height: 70%;
  bottom:0px;
  left:0px;
  overflow:hidden;
  white-space: nowrap;
  animation: bannermove 30s linear infinite;
}
.fog-container img {
  filter: blur(12px);
}

@keyframes bannermove {
  0% {
      transform: translate(0, 0);
  }
  100% {
      transform: translate(-50%, 0);
  }
}

</style>
