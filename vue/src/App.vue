<template>
  <div id="app">
    <div id="nav" v-if="$store.state.token != ''">
<img id="genre_genie" src="./assets/genie.png" alt="genie">
      <router-link v-bind:to="{ name: 'logout' }" v-if="$store.state.token != ''">Logout</router-link>
       <router-link v-bind:to="{ name: 'recommendation' }" v-if="$store.state.token != ''">Recommended</router-link>
      <router-link v-bind:to="{ name: 'search' }" v-if="$store.state.token != ''">Search</router-link>
      <router-link v-bind:to="{name: 'favorites'}" v-if="$store.state.token != ''">My Favorites</router-link>

    </div>
    <router-view />
  </div>
</template>

<style>
body {
  margin: 0;
  font-family: 'Open Sans', sans-serif;
  font-family: 'Poppins', sans-serif;
}
/*.logo{
    width: 50px;
    cursor: pointer;
    
}*/

h1 {
  font-size: 80px;
  font-weight:800;
  color:#f2f2f2;
}

h2 {
  font-size: 60px;
  color:#f2f2f2;
}

p {
  font-size: 15px;
  color:#f2f2f2;
}

#nav {
  overflow: hidden;
  background-color: #3DCAB1;
  
}

#nav a {
  float: right;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

#nav a:hover {
  background-color: #071C42;
}

hr {
  height: 1px;
  background-color:#3DCAB1;
  opacity: 70%;
  border:none;
}
@media (max-width: 768px) {
  h1 {
    font-size: 40px; 
  }
  h2 {
    font-size: 30px; 
  }
  p {
    font-size: 5px; 
  }
 #nav {
    background-color: #3DCAB1;
    text-align: center;
    
    
    
  }
  #nav a {
    float: right; 
    display: block; 
    margin: 5px 0;
    padding:1% 1%; 
  }
}

#genre_genie{
width: 60px;
margin-left: 10px;
}
</style>