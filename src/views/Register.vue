<template>
    <div class="register">
        <TheHeader />
        <div class="content">
            <h1>Register</h1>
            <form @submit.prevent="handleRegister">
                <div>
                <label for="email">Email:</label>
                <input type="email" id="email" v-model="email" required />
                </div>
                <div>
                <label for="username">Username:</label>
                <input type="text" id="username" v-model="username" required />
                </div>
                <div>
                <label for="password">Password:</label>
                <input type="password" id="password" v-model="password" required />
                </div>
                <div>
                <label for="confirmPassword">Confirm Password:</label>
                <input type="password" id="confirmPassword" v-model="confirmPassword" required />
                </div>
                <button type="submit">Register</button>
            </form>
            <div v-if="errorMessage" class="error">{{ errorMessage }}</div>
        </div>
    </div>
</template>
  
<script>
  import { ref } from 'vue';
//   import axios from 'axios';
  import TheHeader from '../components/TheHeader.vue';
  
  export default {
    name: 'RegisterView',
    components: {
        TheHeader
    },
    setup() {
      const email = ref('');
      const username = ref('');
      const password = ref('');
      const confirmPassword = ref('');
      const errorMessage = ref('');
  
    //   const handleRegister = async () => {
    //     if (password.value !== confirmPassword.value) {
    //       errorMessage.value = 'Passwords do not match';
    //       return;
    //     }
    //     try {
    //       await axios.post('http://localhost:5000/api/auth/register', {
    //         email: email.value,
    //         username: username.value,
    //         password: password.value
    //       });
    //       // 회원가입 성공 후 로그인 페이지로 이동
    //       this.$router.push('/login');
    //     } catch (error) {
    //       errorMessage.value = error.response.data;
    //     }
    //   };
  
      return {
        email,
        username,
        password,
        confirmPassword,
        // handleRegister,
        errorMessage
      };
    }
  };
</script>
  
<style scoped>
  .register {
    text-align: center;
    background-color: gray;
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
  .error {
    color: red;
    margin-top: 10px;
  }
</style>
