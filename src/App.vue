<script>
import { RouterLink, RouterView } from 'vue-router'
import NavBar from '@/components/NavBar.vue'
export default {
  components: {
    NavBar,
  },
}
</script>

<template>
  <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Alatsi&family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
  <NavBar />
  <RouterView />
</template>

<style>
.alatsi-regular {
  font-family: "Alatsi", sans-serif;
  font-weight: 400;
  font-style: normal;
}

.montserrat {
  font-family: "Montserrat", sans-serif;
  font-optical-sizing: auto;
  font-weight: 300;
  font-style: normal;
}
</style>
