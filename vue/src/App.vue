<template>
  <div id="app">
    <the-header />
    <!-- <div id="nav">
      <router-link v-bind:to="{ name: 'home' }">Home</router-link>&nbsp;|&nbsp;
      <router-link
        v-bind:to="{ name: 'logout' }"
        v-if="$store.state.token != ''"
        >Logout</router-link
      >&nbsp;|&nbsp;
      <router-link v-bind:to="{ name: 'Landmark-search' }">Search</router-link>
    </div> -->
    
    <router-view />

    <the-footer />
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";


export default {
  name: "App",
  components: {
    TheHeader,
    TheFooter
      
  },
};
  
</script>,
    TheLandmark

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #f2f4f7;
  margin-top: 0px;
}

router-vue {
  display: flex;
  justify-content: center;
  flex-direction: column;
}
</style>

