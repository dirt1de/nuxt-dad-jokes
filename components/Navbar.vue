<template>
  <div>
    <div class="nav">
      <h1 class="logo">Dad Jokes</h1>
      <div class="links">
        <nuxt-link to="/">Home</nuxt-link>
        <nuxt-link to="/jokes">Jokes</nuxt-link>
        <nuxt-link to="/about">About</nuxt-link>
      </div>
    </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.nav{
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: black;
  color: white;
}

.logo{
  margin-left: 20px;
}

.links{
  width: 300px;
  text-decoration: none;
  display: flex;
  justify-content: space-between;
  padding-right: 20px;
}

a{
  text-decoration: none;
  color: white;
  border: 2px solid white;
  padding: 5px;
  border-radius: 10px;
}
</style>