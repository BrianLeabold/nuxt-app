<template>
  <nav>
    <ul>
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/myservices">Services</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
    </ul>
    <ul class="login">
      <li>
        <nuxt-link to="/">Admin</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/">Login</nuxt-link>
      </li>
    </ul>
  </nav>
</template>
<script>
export default {
  name: 'Navbar'
}
</script>
<style scoped>
nav {
  width: 100%;
  height: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  background: black;
}
ul {
  list-style: none;
  padding: 0;
  margin: 0 0 0 400px;
  display: flex;
  justify-content: center;
  align-items: center;
}
li a {
  text-decoration: none;
  margin: 0 15px;
  color: chocolate;
}
.login {
  margin-left: 250px;
}
</style>