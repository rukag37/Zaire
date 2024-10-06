<script>
export default {
  data() {
    return {
      open: 0
    }
  },

  methods: {
    openLetter() {
      this.open = this.open + 1
    }
  },
}
</script>

<template>
  <link rel="stylesheet"
    href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" />
  <main>
    <div v-if="open == 0">
      <p class="montserrat click">Click me!!</p>
      <img src="@/assets/letter1.png" @click="openLetter">
    </div>
    <img src="@/assets/letter2.png" v-if="open == 1" @click="openLetter">
    <div v-if="open == 2" id="letter">
      <span class="material-symbols-outlined" @click="openLetter">cancel</span>
      <p class="montserrat">HAPPYYYYYYYYYYYY BIRTHDAYYYYYYYY to my best friend! You have such a way with words that I'm not sure how to even start this to live up to your text on my birthday that lowkey brought me to tears. But okay, here we go. You've brought so much light into my life, and you're such an important person. Never let anyone make you feel like you're less than what u truly are. I hope to spend the rest of my life giving u silly advice that hopefully counts for something. I truly hope u have the best day ever because u don't deserve anything less. U deserve to be loved today and every day by everyone. I hope 19 treats u as well as it treated me and even better!!!! It’s so beautiful to watch you grow into a more mature and amazing person after FOUR years together u might not notice it but watching it is truly a privilege. The Jennie to my Lisa, THANK YOUUU for always being yourself I wouldn’t want anything else. On a serious note u mean the world to me. You're such a special person who can brighten even my darkest days and u have the biggest heart. My biggest wish is for strangers to experience what it’s like to have u in their lives so they could feel the same way that I do about u. Now you’re in uni, which is such an important chapter! I hope u grow and become everything you've ever wanted. I know you'll achieve everything u set your mind to and I’ll be cheering for u like I’ve done all these years. I know I can always count on u and I keep that info in a special cozy spot in my heart. I truly feel privileged just to know u and be able to talk with u every day. Here’s to many more years of u and our friendship! 🥂🥂🥂 (also I hope u liked this little website kisses)</p>
    </div>
    <img src="@/assets/letter4.png" v-if="open == 3">
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
  justify-content: center;
  align-items: center;
  text-align: center;
}

img {
  width: 20rem;
}

#letter {
  background-color: #ffffff;
  border-radius: 1rem;
  width: 85%;
  min-height: 85vh;
  height: 85%;
  margin: 2em 0;
  color: black;
}

#letter p {
  padding: 0 1rem 1rem 1rem;
}

.material-symbols-outlined {
  font-size: 2.5rem;
  color: #fec5bb;
  display: flex;
  justify-content: right;
  margin: 0.5rem;
}

.click{
  font-size: 28px;
  color: black;
}
</style>
