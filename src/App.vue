<template>
  <nav>
    <router-link :class="{active: $route.name === 'home'}" to="/">Home</router-link> |
    <router-link :class="{active: $route.name === 'Cart'}" to="/cart">About</router-link>
  </nav>
  <router-view/>
</template>
<script>
export default {
  mounted(){
    this.$store.commit('updateCartFromLocalStorage')
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 10px;
  width: 100%;
  height: 20px;
  background-color: white;
  line-height: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;

    &.active{
      color: #2c3e50;
    }
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.text-center{
  text-align: center;
}
</style>
