<template>
  <div class="home">
    <AppHeader />
    <div class="content">
      <h1>Welcome to the Main Page</h1>
    </div>
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader.vue';

export default {
  name: 'HomeView',
  components: {
    AppHeader
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