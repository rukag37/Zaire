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
      <p class="montserrat">HAPPYYYYYYYYYYYY BIRTHDAYYYYYYYY to my best friend, u have such a way with words that im not sure how im gonna start this to live up to your text on my bday that lowkey brough tears to my eyes but okay here we go. You have brought such light to my life u are such an important person and u should never let people feel like u are less than what u truly are. i hope to spend the rest of the days of my life giving u silly advice that hopefully counts for something. i actually hope u have the best day ever cause u dont deserve anything less, u deserve to be loved today and everyday by everyone. i hope 19 treats u as good as it treat me and even better!!!!!!!! its so beautiful to watch u grow into a more mature and bigger person after FOUR years together like u might not notice but its so beautiful to watch it from the side lines. the jennie to my lisa THANK YOUUU for being yourself always i wouldnt want anything else. okay on a serious note u literally mean the world to me like u are such an important person that really can brighten the darkest days, u are such a big hearted person. my biggest wish for strangers is that everyone could have u in their life so they'd feel like i do about u and know how u are such an incredible person. u are now in uni!! which is such an important character i hope u get to grow and become everything you've ever wanted, i hope and i know u will achieve everything u set your mind to and once again like ive done for all these years ill be cheering for u. i know ill always be able to count on u no matter what and its such a piece of info i save in my heart in a very cozy spot. i really really am a privileged person just to know u and being able to communicate with you everyday. To more years of u and our friendship!! 🥂🥂🥂 (also i hope u liked this little website kisses)</p>
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
}
</style>
