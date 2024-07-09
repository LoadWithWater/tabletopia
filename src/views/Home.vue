<template>
  <div class="home">
    <TheHeader />
    <div class="content">
      <h1>Welcome to the Main Page</h1>
      <img src="../../public/main.png">
    </div>
  </div>
</template>

<script>
  import TheHeader from '../components/TheHeader.vue';

  export default {
    name: 'HomeView',
    components: {
      TheHeader
    }
  };
</script>

<style scoped>
  .home {
    text-align: center;
  }
  .content {
    padding-top: 60px; /* 헤더 높이만큼 패딩 추가 */
  }
</style>