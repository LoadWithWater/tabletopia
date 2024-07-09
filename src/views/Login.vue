<template>
  <div class="login">
    <AppHeader />
    <div class="content">
      <h1>Login</h1>
      <form @submit.prevent="handleLogin">
        <div>
          <label for="username">Username:</label>
          <input type="text" id="username" v-model="username" required />
        </div>
        <div>
          <label for="password">Password:</label>
          <input type="password" id="password" v-model="password" required />
        </div>
        <button type="submit">Login</button>
      </form>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
import AppHeader from '../components/AppHeader.vue';

export default {
  name: 'LoginView',
  components: {
    AppHeader
  },
  setup() {
    const username = ref('');
    const password = ref('');

    const handleLogin = () => {
      console.log('Logging in with', username.value, password.value);
      // 로그인 로직을 여기에 추가합니다.
    };

    return {
      username,
      password,
      handleLogin
    };
  }
};
</script>

<style scoped>
  .login {
    text-align: center;
  }
  .content {
    padding-top: 60px; /* 헤더 높이만큼 패딩 추가 */
  }
  form {
    display: inline-block;
    text-align: left;
  }
  form div {
    margin-bottom: 10px;
  }
  button {
    display: block;
    width: 100%;
  }
</style>