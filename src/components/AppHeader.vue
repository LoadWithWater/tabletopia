<template>
  <header>
    <nav>
      <div class="music-control">
        <button @click="toggleMusic">
          <span v-if="isPlaying">⏸️</span>
          <span v-else>▶️</span>
        </button>
        <audio ref="audio" src="/Title.mp3"></audio>
      </div>
      <router-link to="/">Home</router-link>
      <router-link to="/login">Login</router-link>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      isPlaying: false
    };
  },
  methods: {
    toggleMusic() {
      const audio = this.$refs.audio;
      if (this.isPlaying) {
        audio.pause();
      } else {
        audio.play();
      }
      this.isPlaying = !this.isPlaying;
    }
  }
};
</script>

<style scoped>
header {
  background-color: #333;
  color: white;
  padding: 10px;
  text-align: center;
}
nav {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
}
a {
  color: white;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
.music-control {
  margin-right: auto;
}
button {
  background: none;
  border: none;
  color: white;
  cursor: pointer;
  font-size: 1.5rem;
}
</style>
