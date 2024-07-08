<template>
  <div class="home">
    <AppHeader />
    <h1>Welcome to the Main Page</h1>
  </div>
</template>

<script>
import AppHeader from '@/components/AppHeader.vue';

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
  margin-top: 50px;
}
</style>
