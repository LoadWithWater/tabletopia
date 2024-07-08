<template>
  <header>
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/login">Login</router-link>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'AppHeader'
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
  gap: 20px;
}
a {
  color: white;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
</style>
