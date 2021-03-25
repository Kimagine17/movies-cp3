<template>
<div class="main-container">
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/browse">Browse</router-link> |
      <router-link to="/tickets">Tickets</router-link>
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
          <p><a href = "https://github.com/Kimagine17/movies-cp3">Link to GitHub</a></p>
      </div>
    </div>
  </div><!-- footer -->
  </div><!--  main containter -->
</template>

<style>
* {
  box-sizing: border-box;
}

.footer {
  position: absolute;
  bottom: 0;
  width: 100%;

  display: flex;
  padding-top: 10px;
  padding-bottom: 10px; 
  left: 0;
  background-color: #1b500c;
  color: #ffffff;
  text-align: center;
  justify-content: center;  
}
.footer-items {
    width: 100%;
    justify-content: center; 
}
.footer a {
  text-decoration: none;
  color: black;
}
.link {
  padding: 20px;
}
.main-container {
    min-height: 100vh; /* will cover the 100% of viewport */
    overflow: hidden;
    display: block;
    position: relative;
    padding-bottom: 150px; /* height of your footer */
    width: 100%;
}
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

/* Mobile Styles */
@media only screen and (max-width: 400) {

}
  
/* Tablet Styles */
@media only screen and (min-width: 401) and (max-width: 850px) {
    .footer-items {
        display: flex;
        flex-wrap: wrap;
    }
}
  
/* Desktop Styles */
@media only screen and (min-width: 851px) {
    .footer-items {
        display: flex;
        flex-wrap: wrap;
    }
}


</style>
