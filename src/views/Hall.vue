<template>
  <div class="hall">
    <TheHeader />
    <div class="content">
      <h1>Rooms</h1>
      <div class="roomContainers">
        <form>
            <div class="room"></div>
            <div class="room"></div>
        </form>
        <form>
            <div class="room"></div>
            <div class="room"></div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
  import TheHeader from '../components/TheHeader.vue';

  export default {
    name: 'HallView',
    components: {
      TheHeader
    }
  };
</script>

<style scoped>
    .hall {
        text-align: center;
    }
    .content {
        padding-top: 60px; /* 헤더 높이만큼 패딩 추가 */
    }
    .roomContainers {
        display: flex;
    }
    .room {
        width: 500px;
        height: 300px;
        border: 1px solid black;
        margin: 30px;
    }
</style>