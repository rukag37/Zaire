<script>
export default {
  data() {
    return {
      blew: false
    }
  },

  methods: {
    toggleBlew() {
      return this.blew = true
    }
  },
}
</script>

<template>
  <main>
    <img src="@/assets/cake.gif" alt="Birthday Cake Gif" v-if="!blew" @click="toggleBlew">
    <img src="@/assets/cake.png" alt="Birthday Cake Candles Out" v-else>
  </main>
</template>

<style scoped>
main {
  background-color: #f8edeb;
  width: 100%;
  min-height: 100vh;
  height: 100%;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}

img {
  width: 25rem;
}
</style>
