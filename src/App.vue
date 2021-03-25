<template>
<div class="main-container">
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>

  <div class = "footer"> 
    <div class = "footer-items">
      <div class = "link">
          <p> Phone: 509.942.8132 </p>
      </div>
      <div class = "link">
          <p> Email: kimberlite17@gmail.com </p>
      </div>
      <div class = "link">
          <p><a href = "https://github.com/BYU-CS-260-Winter-2021/lab-3b-grocery-store-Kimagine17">Link to GitHub</a></p>
      </div>
    </div>
  </div><!-- footer -->
  </div><!--  main containter -->
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
