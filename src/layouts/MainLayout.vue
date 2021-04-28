<template>
  <q-layout dark view="hhh lpR fFf">
    <q-header dark elevated>
      <q-tabs
        v-model="tab"
        inline-label
      >
        <!-- <q-route-tab v-for="nav in navs" :key="nav.label" :to="nav.path" :icon="nav.icon" :label="nav.label" /> -->
      </q-tabs>
    </q-header>
    <q-page-container class="bg-grey-5">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

export default {
  data() {
    return {
      tab: 'home',
      navs: [
        { label: 'Home', name: 'home', path: '/', icon: 'home' },
        { label: 'About', name: 'about', path: '/about', icon: 'info' },
      ],
    }
  }
}
</script>
