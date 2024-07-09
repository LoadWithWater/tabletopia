<template>
  <header>
    <nav>
      <div class="home">
        <router-link to="/">Home</router-link>
      </div>
      <div class="player">
        <button @click="toggleMusic">
          <span v-if="isPlaying">⏸️</span>
          <span v-else>▶️</span>
        </button>
        <audio ref="audio" src="/Title.mp3"></audio>
      </div>
      <div class="login">
        <router-link to="/login">Login</router-link>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'TheHeader',
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
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 1000;
  }
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .player, .home, .login {
    flex: 1;
    display: flex;
    align-items: center;
  }
  .home, .player {
    justify-content: left;
  }
  .login {
    justify-content: right;
    padding-right: 20px;
  }
  a {
    color: white;
    text-decoration: none;
    margin: 0 10px;
  }
  a:hover {
    text-decoration: underline;
  }
  button {
    background: none;
    border: none;
    color: white;
    cursor: pointer;
    font-size: 1.5rem;
  }
</style>
