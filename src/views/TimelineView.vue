<script>
import funnyImage from '@/assets/funny.jpg';
import minecraftImage from '@/assets/minecraft.png';
import warImage from '@/assets/war.jpg';

export default {
  data() {
    return {
      events: [
        { date: 'Aug 25, 2020', description: 'When we met', picture: '' },
        { date: 'Jan 21, 2021', description: 'Just me and u left', picture: '' },
        { date: 'Mar, 2021', description: '', picture: funnyImage },
        { date: 'May 14, 2021', description: '<3', picture: '' },
        { date: 'Feb, 2023', description: 'COLD WAR', picture: warImage },
        { date: '2023', description: '', picture: minecraftImage },
        { date: 'Oct 19, 2023', description: 'Lacy and Newt birth', picture: '' },
        { date: 'Now', description: 'We are here now!!', picture: '' },
      ],
      isFullscreen: false,
      fullscreenImage: null,
    };
  },

  methods: {
    showFullscreen(image) {
      this.fullscreenImage = image;
      this.isFullscreen = true;
    },
    closeFullscreen() {
      this.isFullscreen = false;
      this.fullscreenImage = null;
    }
  },
};
</script>

<template>
  <main>
    <div class="timeline montserrat">
      <div v-for="(event, index) in events" :key="index"
        :class="['timeline-item', { 'timeline-item-right': index % 2 === 0 }]">
        <div class="timeline-dot"></div>
        <div class="timeline-date">{{ event.date }}</div>
        <div class="timeline-content">
          <p v-if="event.description != ''">{{ event.description }}</p>
          <img v-if="event.picture != ''" :src="event.picture" @click="showFullscreen(event.picture)">
        </div>
      </div>
    </div>

    <div v-if="isFullscreen" class="fullscreen-modal" @click="closeFullscreen">
      <img :src="fullscreenImage" alt="Fullscreen Image">
    </div>
  </main>
</template>

<style scoped>
main {
  background-color: #f8edeb;
  width: 100%;
  min-height: 100vh;
  height: 100%;
  margin: 0;
  padding: 0 0.5em;
}

.timeline {
  position: relative;
  padding: 20px 0;
  margin: 0 auto;
  max-width: 25rem;
  min-height: 35rem;
}

.timeline::before {
  content: '';
  position: absolute;
  width: 4px;
  background-color: #fcd5ce;
  top: 0;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
}

.timeline-item {
  position: relative;
  margin-bottom: 4rem;
  padding-left: 65%;
}

.timeline-item-right {
  padding-left: 0;
  padding-right: 65%;
  text-align: right;
}

.timeline-dot {
  position: absolute;
  top: 0;
  left: 50%;
  width: 12px;
  height: 12px;
  background-color: #fec5bb;
  border-radius: 50%;
  transform: translateX(-50%);
}

.timeline-date {
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  font-weight: bold;
  background: #fec5bb;
  color: white;
  padding: 2px 8px;
  border-radius: 12px;
  white-space: nowrap;
}

.timeline-content {
  background-color: white;
  padding: 10px;
  border-radius: 6px;
  position: relative;
  border: 1px solid #fec5bb;
}

.timeline-content p {
  margin: 0;
  color: #fec5bb;
}

img {
  width: 6.5rem;
  cursor: pointer;
  transition: transform 0.3s;
  border-radius: 5px;
}

.timeline-item img:hover {
  transform: scale(1.05);
}

.fullscreen-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
  cursor: zoom-out;
}

.fullscreen-modal img {
  height: 20rem;
  width: auto;
  border-radius: 5px;
}
</style>
