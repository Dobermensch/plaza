<template>
  <div id="app">
    <Navigation />
    <div id="content">
      <div id="nav">
        <font-awesome-icon icon="bars" size="lg" />
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </div>
      <router-view />
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Navigation from '@/components/Navigation.vue';

export default Vue.extend({
  components: {
    Navigation,
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  display: flex;
  width: 100%;
  padding-top: 5px;
  padding-bottom: 5px;
  border: 1px solid black;

  // a {
  //   font-weight: bold;
  //   color: #2c3e50;

  //   &.router-link-exact-active {
  //     color: #42b983;
  //   }
  // }
}

#content {
  border: 1px solid black;
  position: relative;
  z-index: 2;
  background-color: white;
  min-height: 1000px;
}

.open {
  transform: translateX(300px);
}
</style>
