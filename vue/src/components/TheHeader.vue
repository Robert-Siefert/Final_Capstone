<template>
  <div class="header">
    <!-- Add the logo as an image here -->

  
<!--      
    <img class="NYSEE" src="../assets/y.png" alt="NYSEE Logo" >  -->
    
    <router-link class="logo" v-bind:to="{ name: 'LandingPage' }"
    
      >  <img class="NYSEE" src="../assets/y.png" alt="NYSEE Logo" > </router-link
    >



<!-- add this inside the div below showModal() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    }, -->





    <nav>
      <ul class="nav_links">
       <li><a href="#"
          ><router-link v-bind:to="{ name: 'About' }">About</router-link></a
        > 
        <li>
          <a href="#"
            ><router-link v-bind:to="{ name: 'Landmark-search' }"
              >Search</router-link
            ></a
          >
        </li>

        

        <li class="login">
          <router-link
            v-bind:to="{ name: 'logout' }"
            v-if="$store.state.token == ''"
            >Login</router-link
          >
          <router-link
            v-bind:to="{ name: 'logout' }"
            v-if="$store.state.token != ''"
            >Logout</router-link
          >
        </li>
        <li>
          <router-link
            v-bind:to="{ name: 'LandingPage' }"
            v-if="$store.state.token == ''"
            >Home</router-link
          >
          <router-link
            v-bind:to="{ name: 'home' }"
            v-if="$store.state.token != ''"
            >MyTrips</router-link
          >
        </li>

        <li>
          <h3 class="welcome" v-if="$store.state.token != ''"> <p>Welcome</p>
            {{ $store.state.user.username }}
          </h3>
        </li>
      </ul>
    </nav>

    <div>
      <!-- <p v-if="$store.state.token != ''">
        Welcome {{ $store.state.user.username }}
      </p> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "the-header",
  data() {
    return {
      isModalVisible: false
    };
  },
  showModal() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    },
};
</script>

<style scoped>
 div > .logo .NYSEE {
   max-height: 14vh;
  
 }
.logo {
  cursor: pointer;
  widows: 20px;
  margin-right: auto;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  background-color: #112740;
}

li,
a,
button {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 16px;
  color: #ffffff;
  text-decoration: none;
}

.header {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  /* padding: 30px 10%; */
  max-height: 15vh;
  }
.nav_links {
  list-style: none;
}
.nav_links li {
  display: inline-block;
  padding: 0px 20px;
}
.nav_links li a {
  transition: all 0.3s ease 0s;
}
.nav_links li a:hover {
  color: #0088a9;
}
.welcome:hover {
  color: #0088a9;
}




</style>
